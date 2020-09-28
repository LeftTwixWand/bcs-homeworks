# Задача 1. Информация о типе

## Описание

В презентации к данной лекции был продемонстрирован метод ```DisplayObjectInfo```, который выводил список переменных и свойств для определённого типа.

```cs
public static void DisplayObjectInfo(Object obj)
{
    Type type = obj.GetType();
    Console.WriteLine($"Type: {type.Name}");

    Console.WriteLine($"{Environment.NewLine}Fields:");
    foreach (FieldInfo info in type.GetFields())
    {
        Console.WriteLine($"{info} = {info.GetValue(obj)}");
    }

    Console.WriteLine($"{Environment.NewLine}Properties:");
    foreach (PropertyInfo info in type.GetProperties())
    {
        Console.WriteLine($"{info} = {info.GetValue(obj)}");
    }
}
```

Необходимо расширить этот метод и сделать вывод информации о событиях, конструкторах и методах.
