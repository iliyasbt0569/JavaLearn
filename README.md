## 1. Java JDK жүктеу:
- **1-қадам**: Кез келген интернет браузерін ашып, [Oracle's Java сайт](https://www.oracle.com/java/technologies/javase-downloads.html) немесе [OpenJDK](https://openjdk.java.net/) сайтына өтіңіз.
- **2-қадам**: Өз жүйеңізге сәйкес JDK нұсқасын (Windows, macOS, Linux) таңдаңыз.
- **3-қадам**: JDK нұсқасын жүктеп алыңыз (мысалы, "Download JDK" немесе "Download").
- **4-қадам**: Жүктелген файлды іске қосып, орнатуды аяқтаңыз.

## 2. JDK орнатылғанын тексеру:
- **1-қадам**: Терминал немесе Command Prompt ашыңыз.   Windows (win + r басыңыз және ашылған терезеде төмендегі команданы жазыңыз)
- **2-қадам**: Келесі командамен JDK нұсқасын тексеріңіз. Егер java орнатылған болса версия нөмірі шығады:
```bash
java -version
```

# Зертханалық жұмыс №2.

## Бірінші бағдарлама

``` java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello World");
    }
}
```

## Комментарий
``` java
public class Comments {
    public static void main(String[] args) {
        // Бір жолды комментарий
        System.out.println("Hello, world!"); // БІр жолды, кодтан кейінгі коммендарий
        /*  
            Көпжолды 
        */  
    }
}
```
## Айнымалыны жасау, теңестіру, айнымалының типтері, өрнектер мен операторлар, типтерді түрлендіру
``` java
public class DataTypesAnsVariables {
    public static void main(String[] args) {
        // 1. Айнымалыларды жасау
        // Примитивті типтер
        int myInt = 10;             // Бүтін сан
        double myDouble = 5.5;      // Нақты сан
        char myChar = 'A';          // Символ
        boolean myBoolean = true;   // Логикалық мән
        long myLong = 100000L;      // Ұзын бүтін сан
        float myFloat = 4.5f;       // Жартылай дәлдік нақты сан
        short myShort = 32000;      // Қысқа бүтін сан
        byte myByte = 127;          // Байт түріндегі сан

        // 2. Арифметикалық операторлар
        int sum = myInt + 5;        // Қосу
        int difference = myInt - 3; // Алу
        int product = myInt * 2;    // Көбейту
        int quotient = myInt / 2;   // Бөлу
        int remainder = myInt % 3;  // Қалдықты табу

        // 3. Унарлы операторлар
        myInt++; // Инкремент (1-ге көбейту)
        myInt--; // Декремент (1-ге азайту)
        int negative = -myInt; // Теріс мәнге ауыстыру

        // 4. Салыстыру операторлары
        boolean isEqual = myInt == 10;    // Тең
        boolean isNotEqual = myInt != 10; // Тең емес
        boolean isGreater = myInt > 5;    // Үлкен
        boolean isLess = myInt < 15;      // Кіші
        boolean isGreaterOrEqual = myInt >= 10; // Үлкен немесе тең
        boolean isLessOrEqual = myInt <= 20;    // Кіші немесе тең

        // 5. Логикалық операторлар
        boolean andResult = myBoolean && (myInt > 5); // ЖӘНЕ
        boolean orResult = myBoolean || (myInt < 5);  // НЕМЕСЕ
        boolean notResult = !myBoolean;              // ЕМЕС

        // 6. Биттік операторлар
        int bitAnd = myInt & 5; // Биттік ЖӘНЕ
        int bitOr = myInt | 5;  // Биттік НЕМЕСЕ
        int bitXor = myInt ^ 5; // Биттік ерекшелік НЕМЕСЕ
        int bitShiftLeft = myInt << 2;  // Солға жылжыту
        int bitShiftRight = myInt >> 2; // Оңға жылжыту
        int bitUnsignedRight = myInt >>> 2; // Таңбасыз оңға жылжыту

        // 7. Меншіктеу операторлары
        myInt += 5; // myInt = myInt + 5
        myInt -= 2; // myInt = myInt - 2
        myInt *= 3; // myInt = myInt * 3
        myInt /= 4; // myInt = myInt / 4
        myInt %= 3; // myInt = myInt % 3

        // 8. Тернарлы оператор
        String result = (myInt > 0) ? "Оң сан" : "Теріс сан";

        // 9. Деректерді түрлендіру
        // Автоматты түрлендіру (Widening conversion)
        double convertedDouble = myInt;  // int -> double
        long convertedLong = myInt;     // int -> long

        // Қолмен түрлендіру (Narrowing conversion)
        int convertedInt = (int) myDouble;  // double -> int
        byte convertedByte = (byte) myInt; // int -> byte

        // Мәтінге түрлендіру
        String intToString = Integer.toString(myInt);  // int -> String
        String doubleToString = Double.toString(myDouble); // double -> String

        // Мәтіннен түрлендіру
        int stringToInt = Integer.parseInt("42"); // String -> int
        double stringToDouble = Double.parseDouble("42.5"); // String -> double

        // Нәтижелерді шығару
        System.out.println("Қосу: " + sum);
        System.out.println("Алу: " + difference);
        System.out.println("Көбейту: " + product);
        System.out.println("Бөлу: " + quotient);
        System.out.println("Қалдық: " + remainder);
        System.out.println("Салыстыру нәтижесі: " + isEqual);
        System.out.println("Логикалық ЖӘНЕ: " + andResult);
        System.out.println("Биттік ЖӘНЕ: " + bitAnd);
        System.out.println("Тернарлы нәтиже: " + result);

        // Түрлендіру нәтижелері
        System.out.println("Автоматты түрлендіру (int -> double): " + convertedDouble);
        System.out.println("Автоматты түрлендіру (int -> long): " + convertedLong);
        System.out.println("Қолмен түрлендіру (double -> int): " + convertedInt);
        System.out.println("Қолмен түрлендіру (int -> byte): " + convertedByte);
        System.out.println("int -> String түрлендіру: " + intToString);
        System.out.println("double -> String түрлендіру: " + doubleToString);
        System.out.println("String -> int түрлендіру: " + stringToInt);
        System.out.println("String -> double түрлендіру: " + stringToDouble);
    }
}
```


# Зертханалық жұмыс №3. 

## Басқару құрылымдары. Үзіліс, өту және қайтару операторлары, Шартты операторлар. Тармақталу және таңдау операторлары

``` java
public class JavaControlStructures {
    public static void main(String[] args) {
        // 1. Шартты операторлар (if, if-else, else if)
        int age = 25;
        if (age < 18) {
            System.out.println("Сіз кәмелет жасына толмағансыз.");
        } else if (age >= 18 && age < 65) {
            System.out.println("Сіз жұмыс жасындағы адамсыз.");
        } else {
            System.out.println("Сіз зейнет жасындағы адамсыз.");
        }

        // 2. Таңдау операторлары (switch-case)
        int dayOfWeek = 3; // 1 - Дүйсенбі, 2 - Сейсенбі, т.б.
        switch (dayOfWeek) {
            case 1:
                System.out.println("Бүгін дүйсенбі.");
                break;
            case 2:
                System.out.println("Бүгін сейсенбі.");
                break;
            case 3:
                System.out.println("Бүгін сәрсенбі.");
                break;
            case 4:
                System.out.println("Бүгін бейсенбі.");
                break;
            case 5:
                System.out.println("Бүгін жұма.");
                break;
            case 6:
                System.out.println("Бүгін сенбі.");
                break;
            case 7:
                System.out.println("Бүгін жексенбі.");
                break;
            default:
                System.out.println("Күн нөмірі дұрыс емес!");
                break;
        }

        // 3. Үзіліс (break) және өту (continue) операторлары
        System.out.println("Үзіліс және өту операторлары:");
        for (int i = 1; i <= 10; i++) {
            if (i == 5) {
                System.out.println("5 мәнінде цикл үзіледі.");
                break; // Циклді тоқтату
            }
            if (i % 2 == 0) {
                continue; // Жұп сандарды өткізіп жіберу
            }
            System.out.println("Цикл мәні: " + i);
        }

        // 4. Қайтару (return) операторы
        System.out.println("Қайтару операторының мысалы:");
        int number = 7;
        boolean isEven = checkEven(number); // Функцияны шақыру
        System.out.println(number + " саны жұп па? " + isEven);

        // 5. Тармақталу және таңдау операторлары
        System.out.println("Тармақталу және таңдау операторлары:");
        int num = -5;
        String result = (num > 0) ? "Оң сан" : "Теріс сан"; // Тернарлы оператор
        System.out.println("Сан: " + num + " (" + result + ")");

        // Қосымша мысалдар
        int grade = 85;
        switch (grade / 10) {
            case 10:
            case 9:
                System.out.println("Баға: Өте жақсы");
                break;
            case 8:
                System.out.println("Баға: Жақсы");
                break;
            case 7:
                System.out.println("Баға: Қанағаттанарлық");
                break;
            case 6:
                System.out.println("Баға: Төмен");
                break;
            default:
                System.out.println("Баға: Өте төмен");
                break;
        }
    }

    // Функция: жұп санды тексеру
    public static boolean checkEven(int num) {
        return num % 2 == 0; // Жұп болса, true қайтарады
    }
}

```


# Зертханалық жұмыс №4. 

## Java тілінде циклдік операторлармен жұмыс істеу

``` java
public class LoopExamples {
    public static void main(String[] args) {
        // 1. while циклдік операторы
        System.out.println("while циклдік операторы:");
        int count = 0; // Айнымалыны инициализациялау
        while (count < 5) { // Шарт тексеріледі
            System.out.println("count мәні: " + count);
            count++; // Айнымалыны 1-ге арттыру
        }

        // 2. do-while циклдік операторы
        System.out.println("\ndo-while циклдік операторы:");
        count = 0; // Айнымалыны қайта инициализациялау
        do {
            System.out.println("count мәні: " + count);
            count++;
        } while (count < 5); // Шарт циклден кейін тексеріледі

        // 3. for циклдік операторы
        System.out.println("\nfor циклдік операторы:");
        for (int i = 0; i < 5; i++) { // Циклдың барлық элементтері бір жолда жазылған
            System.out.println("i мәні: " + i);
        }

        // 4. Циклдық операторларды салыстыру
        System.out.println("\nЦиклдық операторларды салыстыру:");
        System.out.println("1) while: Шарт циклдің алдында тексеріледі, шарт дұрыс болмаса, цикл орындалмайды.");
        System.out.println("2) do-while: Шарт циклден кейін тексеріледі, ең болмағанда бір рет орындалады.");
        System.out.println("3) for: Циклдың барлық элементтері (инициализация, шарт, арттыру/азайту) бір жерде көрсетіледі.");

        // 5. Циклдарды жүзеге асыру
        System.out.println("\nЦиклдарды жүзеге асыру:");
        System.out.println("1-ден 10-ға дейінгі сандардың қосындысын табу:");
        int sum = 0;
        for (int i = 1; i <= 10; i++) {
            sum += i; // Әрбір санды қосу
        }
        System.out.println("Қосынды: " + sum);

        // 6. Циклдық операторлармен жұмыс
        System.out.println("\nЦиклдық операторлармен жұмыс:");
        System.out.println("Тақ сандарды басып шығару (1-ден 10-ға дейін):");
        for (int i = 1; i <= 10; i++) {
            if (i % 2 != 0) { // Тақ санды тексеру
                System.out.println("Тақ сан: " + i);
            }
        }
    }
}

```


# Зертханалық жұмыс №5.

## Java тілінде деректердің күрделі типтері және массивтермен жұмыс
``` java
public class ComplexDataTypes {
    public static void main(String[] args) {
        // 1. Бірөлшемді массивтер
        // Бірөлшемді массивті анықтау
        int[] oneDimensionalArray = {1, 2, 3, 4, 5};

        // Массив элементтеріне қол жеткізу
        System.out.println("Бірөлшемді массив элементтері:");
        for (int i = 0; i < oneDimensionalArray.length; i++) {
            System.out.println("Элемент [" + i + "] = " + oneDimensionalArray[i]);
        }

        // 2. Көпөлшемді массивтер
        // Екіөлшемді массивті анықтау
        int[][] twoDimensionalArray = {
            {1, 2, 3},
            {4, 5, 6},
            {7, 8, 9}
        };

        // Екіөлшемді массив элементтеріне қол жеткізу
        System.out.println("\nЕкіөлшемді массив элементтері:");
        for (int i = 0; i < twoDimensionalArray.length; i++) {
            for (int j = 0; j < twoDimensionalArray[i].length; j++) {
                System.out.print("Элемент [" + i + "][" + j + "] = " + twoDimensionalArray[i][j] + "  ");
            }
            System.out.println();
        }

        // 3. Күрделі типтермен жұмыс
        // Жолдардың массиві (String[])
        String[] names = {"Али", "Бек", "Гүлжан", "Айгүл"};
        System.out.println("\nАттар массиві:");
        for (String name : names) {
            System.out.println(name);
        }

        // Объектілер массиві
        Person[] people = {
            new Person("Али", 25),
            new Person("Бек", 30),
            new Person("Гүлжан", 22)
        };

        System.out.println("\nОбъектілер массиві:");
        for (Person person : people) {
            System.out.println(person.getName() + ", Жасы: " + person.getAge());
        }

        // 4. Массивтермен қосымша операциялар
        // Массивтің ең үлкен элементін табу
        int max = oneDimensionalArray[0];
        for (int num : oneDimensionalArray) {
            if (num > max) {
                max = num;
            }
        }
        System.out.println("\nБірөлшемді массивтің ең үлкен элементі: " + max);

        // Екіөлшемді массивтің элементтерін транспозициялау
        System.out.println("\nЕкіөлшемді массивтің транспозициясы:");
        for (int i = 0; i < twoDimensionalArray[0].length; i++) {
            for (int j = 0; j < twoDimensionalArray.length; j++) {
                System.out.print(twoDimensionalArray[j][i] + "  ");
            }
            System.out.println();
        }
    }
}

// Объектілер массиві үшін "Person" класы
class Person {
    private String name;
    private int age;

    // Конструктор
    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    // Getter әдістері
    public String getName() {
        return name;
    }

    public int getAge() {
        return age;
    }
}

```


# Зертханалық жұмыс №6.

## Жолдар және жолдармен жұмыс істеу әдістері
``` java
public class StringOperations {
    public static void main(String[] args) {
        // 1. Жол жасау
        String firstString = "Сәлем, Әлем!"; // Жолды жасау
        String secondString = "Java бағдарламалау"; // Екінші жол

        // 2. Жолдарды біріктіру
        String combinedString = firstString + " " + secondString; // Жолдарды біріктіру
        System.out.println("Жолдарды біріктіру: " + combinedString);

        // 3. Жол ұзындығын табу
        int length = firstString.length(); // Жолдың ұзындығын алу
        System.out.println("Бірінші жолдың ұзындығы: " + length);

        // 4. Жолдан символ алу
        char firstChar = firstString.charAt(0); // Бірінші символды алу
        System.out.println("Бірінші символ: " + firstChar);

        // 5. Жолды кіші және үлкен әріпке ауыстыру
        String upperCase = firstString.toUpperCase(); // Үлкен әріптерге ауыстыру
        String lowerCase = firstString.toLowerCase(); // Кіші әріптерге ауыстыру
        System.out.println("Үлкен әріптер: " + upperCase);
        System.out.println("Кіші әріптер: " + lowerCase);

        // 6. Жолды салыстыру
        boolean isEqual = firstString.equals(secondString); // Толық салыстыру
        boolean isIgnoreCaseEqual = firstString.equalsIgnoreCase("сәлем, әлем!"); // Регистрді ескерусіз салыстыру
        System.out.println("Жолдар тең бе? " + isEqual);
        System.out.println("Регистрді ескерусіз тең бе? " + isIgnoreCaseEqual);

        // 7. Жолдың бір бөлігін табу
        boolean containsWord = secondString.contains("бағдарламалау"); // Сөздің бар-жоғын тексеру
        int indexOfWord = secondString.indexOf("бағдарламалау"); // Сөздің индексін табу
        System.out.println("Сөз бар ма? " + containsWord);
        System.out.println("Сөздің индексі: " + indexOfWord);

        // 8. Жолдан бөлікті алу
        String substring = secondString.substring(5, 15); // 5-тен 15-ке дейінгі бөлікті алу
        System.out.println("Жолдың бір бөлігі: " + substring);

        // 9. Жолды бөлу
        String[] words = secondString.split(" "); // Жолды бос орындар бойынша бөлу
        System.out.println("Жолды бөлу:");
        for (String word : words) {
            System.out.println(word);
        }

        // 10. Жолды алмастыру
        String replacedString = secondString.replace("бағдарламалау", "программалау"); // Сөзді алмастыру
        System.out.println("Алмастырылған жол: " + replacedString);

        // 11. Жолды бос орындардан тазарту
        String stringWithSpaces = "   Java бағдарламалау   ";
        String trimmedString = stringWithSpaces.trim(); // Бастапқы және соңғы бос орындарды жою
        System.out.println("Бос орындардан тазартылған жол: '" + trimmedString + "'");

        // 12. Бос жолды тексеру
        String emptyString = ""; // Бос жол
        boolean isEmpty = emptyString.isEmpty(); // Жол бос па?
        System.out.println("Жол бос па? " + isEmpty);

        // 13. Null мәнді тексеру
        String nullString = null; // Null мән
        boolean isNull = (nullString == null); // Null мән екенін тексеру
        System.out.println("Жол null мән бе? " + isNull);

        // 14. Жолды мәнге түрлендіру
        int number = 123;
        String numberString = String.valueOf(number); // Бүтін санды жолға түрлендіру
        System.out.println("Санды жолға түрлендіру: " + numberString);
    }
}

```


# Зертханалық жұмыс №7.

## Java объектілі моделі. ОББ-ға кіріспе. ОББ-ның негізгі принциптері.
``` java
// Java ортасындағы ОББ. Класстар мен әдістерді сипаттау. Класс конструкторлары

// ОББ (Объектілі Бағдарламалау Бағдарламасы) негізгі принциптері:
// 1. Инкапсуляция (Encapsulation)
// 2. Мұрагерлік (Inheritance)
// 3. Полиморфизм (Polymorphism)
// 4. Абстракция (Abstraction)

// Негізгі классты құру
class Animal {
    // 1. Дала (Fields) – объектінің қасиеттері
    private String name;  // Жануардың аты
    private int age;      // Жануардың жасы

    // 2. Конструктор – объектіні инициализациялау
    public Animal(String name, int age) {
        this.name = name; // this.name – класстың өрісі
        this.age = age;
    }

    // 3. Геттер мен Сеттер (Getters and Setters) – инкапсуляцияны қамтамасыз етеді
    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }

    // 4. Әдіс (Method) – объектінің әрекеті
    public void makeSound() {
        System.out.println(name + " дыбыс шығарады.");
    }

    // 5. Объект туралы ақпаратты шығару
    @Override
    public String toString() {
        return "Жануардың аты: " + name + ", жасы: " + age;
    }
}

// "Dog" классы "Animal" класынан мұра алады (Inheritance)
class Dog extends Animal {
    private String breed; // Иттің тұқымы

    // Конструктор
    public Dog(String name, int age, String breed) {
        super(name, age); // Супер класс (Animal) конструкторын шақыру
        this.breed = breed;
    }

    // Итке арналған ерекше әдіс
    public void fetch() {
        System.out.println(getName() + " доп әкеліп жатыр!");
    }

    @Override
    public void makeSound() {
        System.out.println(getName() + " үреді!");
    }

    @Override
    public String toString() {
        return super.toString() + ", тұқымы: " + breed;
    }
}

// Бағдарламаны орындау үшін негізгі класс
public class Main {
    public static void main(String[] args) {
        // 1. Объектілерді құру
        Animal animal = new Animal("Жануар", 5);
        Dog dog = new Dog("Бобик", 3, "Лабрадор");

        // 2. Әр объектінің әдістерін шақыру
        System.out.println(animal.toString());
        animal.makeSound();

        System.out.println(dog.toString());
        dog.makeSound();
        dog.fetch();

        // 3. Инкапсуляцияны тексеру
        animal.setName("Жаңа жануар");
        animal.setAge(6);
        System.out.println("Жаңартылған ақпарат: " + animal);

        // 4. Полиморфизмді көрсету
        Animal polymorphicAnimal = new Dog("Шарик", 2, "Пудель");
        polymorphicAnimal.makeSound(); // Иттің "үреді!" деген ерекше әрекеті орындалады
    }
}

```


# Зертханалық жұмыс №8.

## Java-да I/O ұйымдастырудың ағындық моделі. InputStream және OutputStream класстары. Файлдармен жұмыс
``` java
// Java ортасында деректерді енгізу және шығару. Java ортасында I/O ұйымдастырудың моделі
public class JavaIOModel {
    public static void main(String[] args) {
        // 1. InputStream және OutputStream класстары арқылы файлдармен жұмыс істеу
        try {
            // Файлды оқу
            FileInputStream fileInput = new FileInputStream("input.txt");
            int byteRead;
            System.out.println("Файлдан оқу нәтижесі:");

            while ((byteRead = fileInput.read()) != -1) {
                System.out.print((char) byteRead); // Файлдағы символдарды оқу
            }
            fileInput.close(); // Файлды жабу

            System.out.println("\n\n------------------------");

            // Файлға жазу
            FileOutputStream fileOutput = new FileOutputStream("output.txt");
            String data = "Бұл Java-да I/O модельі бойынша жазылатын мәтін.";
            byte[] dataBytes = data.getBytes(); // Мәтінді байттарға түрлендіру
            fileOutput.write(dataBytes); // Файлға жазу

            fileOutput.close(); // Файлды жабу
            System.out.println("Файлға жазу аяқталды. 'output.txt' файлында жазылған мәтін бар.");

        } catch (IOException e) {
            e.printStackTrace(); // Егер қате болса, қате туралы ақпарат шығару
        }

        System.out.println("\n------------------------");
        
        // 2. BufferedInputStream және BufferedOutputStream
        try {
            // Файлдан деректерді буферлі оқу
            FileInputStream fileInputBuffered = new FileInputStream("input.txt");
            BufferedInputStream bufferedInput = new BufferedInputStream(fileInputBuffered);
            int byteReadBuffered;
            System.out.println("Буфер арқылы оқу нәтижесі:");

            while ((byteReadBuffered = bufferedInput.read()) != -1) {
                System.out.print((char) byteReadBuffered); // Файлдағы символдарды оқу
            }
            bufferedInput.close(); // Буферді жабу

            System.out.println("\n\n------------------------");

            // Буферлі жазу
            FileOutputStream fileOutputBuffered = new FileOutputStream("outputBuffered.txt");
            BufferedOutputStream bufferedOutput = new BufferedOutputStream(fileOutputBuffered);
            String dataBuffered = "Буфер арқылы жазылатын мәтін.";
            byte[] dataBytesBuffered = dataBuffered.getBytes(); // Мәтінді байттарға түрлендіру
            bufferedOutput.write(dataBytesBuffered); // Буферге жазу

            bufferedOutput.close(); // Буферді жабу
            System.out.println("Буфер арқылы жазу аяқталды. 'outputBuffered.txt' файлында жазылған мәтін бар.");

        } catch (IOException e) {
            e.printStackTrace(); // Егер қате болса, қате туралы ақпарат шығару
        }
        
        System.out.println("\n------------------------");

        // 3. FileReader және FileWriter класстары арқылы мәтіндік файлдармен жұмыс
        try {
            // FileReader арқылы файлдан оқу
            FileReader fileReader = new FileReader("input.txt");
            int charRead;
            System.out.println("FileReader арқылы оқу нәтижесі:");

            while ((charRead = fileReader.read()) != -1) {
                System.out.print((char) charRead); // Файлдағы символдарды оқу
            }
            fileReader.close(); // Файлды жабу

            System.out.println("\n\n------------------------");

            // FileWriter арқылы файлға жазу
            FileWriter fileWriter = new FileWriter("outputFileWriter.txt");
            String textToWrite = "FileWriter класы арқылы жазылатын мәтін.";
            fileWriter.write(textToWrite); // Файлға жазу
            
            fileWriter.close(); // Файлды жабу
            System.out.println("FileWriter арқылы жазу аяқталды. 'outputFileWriter.txt' файлында жазылған мәтін бар.");

        } catch (IOException e) {
            e.printStackTrace(); // Егер қате болса, қате туралы ақпарат шығару
        }
        
        System.out.println("\n------------------------");
        
        // 4. BufferedReader және BufferedWriter класы арқылы мәтіндік файлдармен жұмыс
        try {
            // BufferedReader арқылы файлдан оқу
            FileReader bufferedFileReader = new FileReader("input.txt");
            BufferedReader bufferedReader = new BufferedReader(bufferedFileReader);
            String line;
            System.out.println("BufferedReader арқылы оқу нәтижесі:");

            while ((line = bufferedReader.readLine()) != null) {
                System.out.println(line); // Файлдағы әрбір жолды оқу
            }
            bufferedReader.close(); // Буферді жабу

            System.out.println("\n\n------------------------");

            // BufferedWriter арқылы файлға жазу
            FileWriter bufferedFileWriter = new FileWriter("outputBufferedWriter.txt");
            BufferedWriter bufferedWriter = new BufferedWriter(bufferedFileWriter);
            String textBufferedWriter = "BufferedWriter класы арқылы жазылатын мәтін.";
            bufferedWriter.write(textBufferedWriter); // Буферге жазу
            
            bufferedWriter.close(); // Буферді жабу
            System.out.println("BufferedWriter арқылы жазу аяқталды. 'outputBufferedWriter.txt' файлында жазылған мәтін бар.");

        } catch (IOException e) {
            e.printStackTrace(); // Егер қате болса, қате туралы ақпарат шығару
        }
        
        System.out.println("\n------------------------");

        // 5. PrintWriter класы арқылы файлға жазу
        try {
            PrintWriter printWriter = new PrintWriter("outputPrintWriter.txt");
            printWriter.println("PrintWriter класы арқылы жазылатын мәтін.");
            printWriter.println("Бұл жол PrintWriter класы арқылы жазылған.");
            printWriter.close(); // Файлды жабу
            System.out.println("PrintWriter арқылы жазу аяқталды. 'outputPrintWriter.txt' файлында жазылған мәтін бар.");
        } catch (IOException e) {
            e.printStackTrace(); // Егер қате болса, қате туралы ақпарат шығару
        }
    }
}

```


# Зертханалық жұмыс №9.

## Java тілінде көп ағынды бағдарламалау: Ағындарды жасау, басқару және синхронизациялау
``` java
public class MultiThreadingExample {
    public static void main(String[] args) {
        // 1. Ағындарды жасау (Thread класын пайдалану)
        Thread thread1 = new Thread(new MyRunnable()); // Ағын 1
        Thread thread2 = new Thread(new MyRunnable()); // Ағын 2

        // 2. Ағындарды іске қосу
        thread1.start(); 
        thread2.start(); 

        try {
            // 3. Ағындардың аяқталуын күту
            thread1.join(); 
            thread2.join(); 
        } catch (InterruptedException e) {
            e.printStackTrace();
        }

        System.out.println("Екі ағын да аяқталды.");
    }
}

// 4. Ағындарды жүзеге асыратын класс
class MyRunnable implements Runnable {
    @Override
    public void run() {
        for (int i = 0; i < 5; i++) {
            System.out.println(Thread.currentThread().getName() + " есептеу: " + i);
            try {
                Thread.sleep(500); // 0.5 секундке үзіліс
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        }
    }
}

```
