# Python

## Notes

- Можно загрузить готовый код на [Pastebin](http://pastebin.org/)
- Использовать автоматическое форматирование текста  [Pythonbuddy](https://pythonbuddy.com/)
- Использовать playgrounds:
    - html, css, js - [jsfiddle](https://jsfiddle.net/) или [playcode](https://playcode.io/)
    - php, phyton, c++ - [replit](https://replit.com/)
    - SQL - [sqlfiddle](http://sqlfiddle.com/)

## Python код в .exe

1. Установить pyinstaller с помощью pip:
   
    ```
    pip install pyinstaller
    ```
    
    При использовании Linux:
    
    ```
    apt-get install python-pip
    ```
    
2. Формируем исполнительный .exe файл: 

    ```
    pyinstaller -F -w -i( to set up icon on your .exe) main.py
    ```

    F – в созданной папке dist, в которой и будет храниться исполняемый файл не будет лишних файлов, модулей и т.п.

    w – если приложение использует tkinekt, оно блокирует создание консольного окна, если приложение консольное, этот флаг использовать не нужно

    i – установка иконки на исполняемый файл, после флага указать полный путь к иконке с указанием её имени

3. Пример:

    ```
    pyinstaller -F -w -i C:\Users\AZT\Desktop\ICON.ico hrequest.pyw
    ```

## Запись в CSV при помощи DictWriter

    def csv_dict_writer(path, fieldnames, data):
      with open(path, "w", newline='') as out_file:
            writer = csv.DictWriter(out_file, delimiter=',', fieldnames=fieldnames)
            writer.writeheader()
            for row in data:
                writer.writerow(row)
               
    if __name__ == "__main__":
        data = ["first_name,last_name,city".split(","),
                "Tyrese,Hirthe,Strackeport".split(","),
                "Jules,Dicki,Lake Nickolasville".split(","),
                "Dedric,Medhurst,Stiedemannberg".split(",")
                ]
    
        my_list = []
        fieldnames = data[0]
        for values in data[1:]:
            inner_dict = dict(zip(fieldnames, values))
            my_list.append(inner_dict)
    
        path = "dict_output.csv"
        csv_dict_writer(path, fieldnames, my_list)


​    

