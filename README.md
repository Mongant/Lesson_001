# Lesson_001

### Создание jar файла и компиляция java class через терминал
Собираем архив, который можно запускать с помощью команды java -jar <имя архива>. Для начала создаем файл manifest.mf, в котором будет указан главный исполняемый класс:
```
Manifest-Version: 1.0
Created-By: 1.6.0_19 (Sun Microsystems Inc.)
Main-Class: mypackage.HelloWorld
```
Выполняем команду по сборке архива:
```
jar cvmf manifest.mf helloWorld.jar -C ./classes mypackage
```
В результате должен быть создан файл helloWorld.jar со следующей структурой
```
META-INF/MANIFEST.MF
mypackage/HelloWorld.class
```

### Выполнение программы запуском jar-файла

```
java -jar helloWorld.jar
```
