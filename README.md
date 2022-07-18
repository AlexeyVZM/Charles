# Charles
Charles HW Traffic capture

Ex_0: Сфокусироваться на ниже перечисленных запросах

Protocol: http
IP: 162.55.220.72
Port: 5005

Ex_1: 
Method: GET
EndPoint: /get_method
request url params: 
 name: str
 age: int

response: 
[
    “Str”,
    “Str”
]

Task:
Сделать в Rewrite
 ⁃ Подменить url в Charles чтобы в запросе ушло имя которые вы вписали в Postman, а вернулось то, которое вы подставили в Charles.
 
Подмена URL через Charles:
![Подмена URL через Charles](https://github.com/AlexeyVZM/Charles/blob/main/1_rewrite_param_name(charles).jpg)

Смотрим, как отработался запрос с измененным URL в Postman
![Смотрим, как отработался запрос с измененным URL в Postman](https://github.com/AlexeyVZM/Charles/blob/main/1_rewrite_param_name(postman).jpg)

==================

Ex_2:
Method: POST
EndPoint: /user_info_3
request form data: 
 name: str
 age: int
 salary: int

response: 
{'name': name,
          'age': age,
          'salary': salary,
          'family': {'children': [['Alex', 24], ['Kate', 12]],
                     'u_salary_1_5_year': salary * 4}}

Task:
Сделать в Rewrite
 ⁃ Подменить body в Charles так чтобы в запросе ушла salary которую вы вписали в Postman, а в u_salary_1_5_year цифра вернулась меньше оригинальной из запроса.

Подмена body через Charles:
![Подмена body через Charles](https://github.com/AlexeyVZM/Charles/blob/main/2_rewrite_param_salary(charles).jpg)

Смотрим, как отработался запрос с измененным body в Postman
![Смотрим, как отработался запрос с измененным body в Postman](https://github.com/AlexeyVZM/Charles/blob/main/2_rewrite_param_salary(postman).jpg)


==================

Ex_3:
Method: GET
EndPoint: /object_info_1
request url params: 
 name: str
 age: int
 weight: int

response: 
{'name': name,
          'age': age,
          'daily_food': weight * 0.012,
          'daily_sleep': weight * 2.5}

Task:
Сделатьв Rewrite
 ⁃ Подменить параметры запроса в Charles так, чтобы в Postman пришел ответ где другое name, daily_food > weight из запроса, а daily_sleep < weight из запроса.
