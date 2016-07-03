FORMAT: 1A

# Gestión de exámenes

Documentación para la API MPWAR

# Group Examen

# Examen [/exams]

## Crear nuevo [POST]

+ Request (application/json)

  + Body

    ```
      {
        "name": "prueba MPWAR",
        "instructions": "instrucciones van aqui",
        "duration": 50,
        "extra_time": 5,
        "is_active": true,
        "is_autocorrect": false,
        "id_user": 6
      }
    ```

+ Response 200 (application/json)

  + Body

    ```
      {
        "code": 200,
        "message": "OK"
      }
    ```

# Examen [/exams]

## Obtener todos [GET]

+ Response 200 (application/json)

  + Body

    ```
      [{
        "id_test": "test10318",
        "name": "prueba MPWAR",
        "instructions": "instrucciones van aqui",
        "duration": 50,
        "extra_time": 5,
        "id_user": {
          "id": 6,
          "company_id": {
            "id": 1,
            "name": "Company For Test",
            "created_at": "2016-04-11T22:03:21+0200"
          },
          "rol_id": {
            "id": 1,
            "name": "Manager",
            "created_at": "2016-04-11T22:03:21+0200"
          },
          "name": "Victor",
          "lastname": "Perez",
          "email": "vp@gmail.com",
          "password": "$2y$10$HHU.Kp1Rr5UUiRtCdandhOEIouruSqbACfuE267xxsK4uc\/MniQxS",
          "is_active": true,
          "created_at": "2016-06-10T12:52:45+0200"
        },
        "is_active": true,
        "is_autocorrect": false,
        "created_at": "2016-06-10T17:48:21+0200"
      }]
    ```

# Examen [/exams/id]

## Obtener detalle [GET]

+ Response 200 (application/json)

  + Body

    ```
      {
        "id_test": "test10318",
        "name": "prueba MPWAR",
        "instructions": "instrucciones van aqui",
        "duration": 50,
        "extra_time": 5,
        "id_user": {
          "id": 6,
          "company_id": {
            "id": 1,
            "name": "Company For Test",
            "created_at": "2016-04-11T22:03:21+0200"
          },
          "rol_id": {
            "id": 1,
            "name": "Manager",
            "created_at": "2016-04-11T22:03:21+0200"
          },
          "name": "Victor",
          "lastname": "Perez",
          "email": "vp@gmail.com",
          "password": "$2y$10$HHU.Kp1Rr5UUiRtCdandhOEIouruSqbACfuE267xxsK4uc\/MniQxS",
          "is_active": true,
          "created_at": "2016-06-10T12:52:45+0200"
        },
        "is_active": true,
        "is_autocorrect": false,
        "created_at": "2016-06-10T17:48:21+0200"
      }
    ```

# Examen [/exams/id]

## Modificar [PUT]

+ Request (application/json)

  + Body

    ```
      {
        "id_test": "test10318",
        "name": "prueba MPWAR"
        "instructions": "instrucciones van aqui",
        "duration": 50,
        "extra_time": 5,
        "is_active": true,
        "is_autocorrect": false,
        "id_user": 6
      }
    ```

+ Response 200 (application/json)

  + Body

    ```
      {
        "code": 200,
        "message": "OK"
      }
    ```
# Examen [/exams/id]

## Eliminar [DELETE]

+ Response 200 (application/json)

  + Body

    ```
      {
        "code": 200,
        "message": "OK"
      }
    ```

# Group Tipo de pregunta

# Tipo de pregunta [/questiontypes]

## Crear tipo de pregunta [POST]

+ Request (application/json)

  + Body

    ```
      {
        "description": "Descripcion de tipo de pregunta"
        "autocorrect": false
      }
    ```

+ Response 200 (application/json)

  + Body

    ```
      {
        "code": 200,
        "message": "OK"
      }
    ```

# Tipo de pregunta [/questiontypes]

## Obtener todos los tipos de pregunta [GET]

+ Response 200 (application/json)

  + Body

    ```
      [{
        "id": 1,
        "description": "seleccion simple",
        "autocorrect": true,
        "registration_date": "2015-08-25T22:47:19+0200"
      }]
    ```

# Tipo de pregunta [/questiontypes/id]

## Ver detalle de tipo de pregunta [GET]

+ Response 200 (application/json)

  + Body

    ```
      {
        "id": 1,
        "description": "seleccion simple",
        "autocorrect": true,
        "registration_date": "2015-08-25T22:47:19+0200"
      }
    ```

# Tipo de pregunta [/questiontypes/id]

## Modificar tipo de pregunta [PUT]
+ Request (application/json)

  + Body

    ```
      {
        "description": "Descripcion de tipo de pregunta"
        "autocorrect": true
      }
    ```

+ Response 200 (application/json)

  + Body

    ```
      {
        "code": 200,
        "message": "OK"
      }
    ```

# Tipo de pregunta [/questiontypes/id]

## Eliminar tipo de pregunta [DELETE]

+ Response 200 (application/json)

  + Body

    ```
      {
        "code": 200,
        "message": "OK"
      }
    ```

# Pregunta [/questions]

## Crear pregunta [POST]
+ Request (application/json)

  + Body

    ```
      [{
        "question_number" : 1,
        "id_type" : 1,
        "id_test" : "test9699",
        "description" : "Descripcion 1",
        "score" : 20
      }]
    ```

+ Response 200 (application/json)

  + Body

    ```
      {
        "code": 200,
        "message": "OK"
      }
    ```

# Pregunta [/questions]

## Obtener todas las preguntas [GET]

+ Response 200 (application/json)

  + Body

    ```
      [{
        "id": 54,
        "type": {
          "id": 1,
          "description": "seleccion simple",
          "autocorrect": true,
          "registration_date": "2015-08-25T22:47:19+0200"
        },
        "id_test": "test10318",
        "description": "Pregunta 1",
        "score": 20,
        "created_at": "2016-06-15T11:49:17+0200"
      }]
    ```

# Pregunta [/questions/id]

## Ver detalle de pregunta [GET]

+ Response 200 (application/json)

  + Body

    ```
      {
        "id": 54,
        "type": {
          "id": 1,
          "description": "seleccion simple",
          "autocorrect": true,
          "registration_date": "2015-08-25T22:47:19+0200"
        },
        "id_test": "test10318",
        "description": "Pregunta 1",
        "score": 20,
        "created_at": "2016-06-15T11:49:17+0200"
      }
    ```

# Pregunta [/questions/id]

## Modificar pregunta [PUT]

+ Request (application/json)
    
  + Body

    ```
      [{
        "id": 54,
        "type": {
          "id": 1,
          "description": "seleccion simple",
          "autocorrect": true,
          "registration_date": "2015-08-25T22:47:19+0200"
        },
        "id_test": "test10318",
        "description": "Pregunta 1",
        "score": 10,
        "created_at": "2016-06-15T11:49:17+0200"
      }]
    ```

+ Response 200 (application/json)

```
  {
    "code": 200,
    "message": "OK"
  }
```

# Pregunta [/questions/id]

## Eliminar pregunta [DELETE]

+ Response 200 (application/json)
  
  + Body

    ```
      {
        "code": 200,
        "message": "OK"
      }
    ```

# Group Pregunta propuesta

# Pregunta propuesta [/proposedanswers]

## Crear pregunta propuesta [POST]

+ Request (application/json)

  + Body

  ```
    [{
      "id_question": 2,
      "answer": "Respuesta propuesta a pregunta",
      "is_correct": true,
      "score": 5,
      "file": "none"
    }]
  ```

+ Response 200 (application/json)

```
  {
    "code": 200,
    "message": "OK"
  }
```

# Pregunta propuesta [/proposedanswers]

## Obtener todas las respuestas propuestas a preguntas [GET]

+ Response 200 (application/json)

  + Body

    ```
      [{
        "id": 5,
        "id_question": 2,
        "answer": "Respuesta propuesta a pregunta",
        "is_correct": true,
        "score": 5,
        "file": "none"
      }]
    ```

# Pregunta propuesta [/proposedanswers/id]

## Ver detalle de respuesta propuesta a pregunta [GET]

+ Response 200 (application/json)

  + Body

    ```
      {
        "id": 54,
        "type": {
          "id": 1,
          "description": "seleccion simple",
          "autocorrect": true,
          "registration_date": "2015-08-25T22:47:19+0200"
        },
        "id_test": "test10318",
        "description": "Pregunta 1",
        "score": 20,
        "created_at": "2016-06-15T11:49:17+0200"
      }
    ```

# Pregunta propuesta [/proposedanswers/id]

## Modificar respuesta propuesta [PUT]
+ Request (application/json)

  + Body

  ```
    [{
      "id": 54,
      "type": {
        "id": 1,
        "description": "seleccion simple",
        "autocorrect": true,
        "registration_date": "2015-08-25T22:47:19+0200"
      },
      "id_test": "test10318",
      "description": "Pregunta 1",
      "score": 10,
      "created_at": "2016-06-15T11:49:17+0200"
    }]
  ```

+ Response 200 (application/json)

  + Body

    ```
      {
        "code": 200,
        "message": "OK"
      }
    ```

# Pregunta propuesta [/proposedanswers/id]

## Eliminar respuesta propuesta a pregunta [DELETE]

+ Response 200 (application/json)

  + Body

    ```
      {
        "code": 200,
        "message": "OK"
      }
    ```

# Group Corregir Examen

# Corregir examen [/reviewertests]

## Crear nuevo [POST]

+ Request (application/json)

  + Body

    ```
      {
        "id_test": "test18707",
        "id_reviewer": 5
      }
    ```

+ Response 200 (application/json)

  + Body

    ```
      {
        "code": 200,
        "message": "OK"
      }
    ```

# Corregir examen [/reviewertests]

## Obtener todos [GET]

+ Response 200 (application/json)

  + Body

    ```
      {
        "raw": [{
          "id": 1,
          "id_user": 4,
          "id_test": "test3129",
          "created_at": "2016-06-27T19:07:13+0200"
        }],
        "tests": [{
          "id_test": "test3129",
          "name": "prueba",
          "instructions": "hola",
          "duration": 5,
          "extra_time": 5,
          "id_user": {
            "id": 4,
            "company_id": {
              "id": 1,
              "name": "Company For Test",
              "created_at": "2016-04-11T22:03:21+0200"
            },
            "rol_id": {
              "id": 1,
              "name": "Manager",
              "created_at": "2016-04-11T22:03:21+0200"
            },
            "name": "Postman 22",
            "lastname": "Chrome 22",
            "email": "pchrome22@gmail.com",
            "password": "$2y$10$HHU.Kp1Rr5UUiRtCdandhOEIouruSqbACfuE267xxsK4uc/MniQxS",
            "is_active": true,
            "created_at": "2016-06-10T12:52:45+0200"
          },
          "is_active": true,
          "is_autocorrect": false,
          "created_at": "2016-06-24T19:27:32+0200"
        }]
      }
    ```

# Corregir Examen [/reviewertests/id]

## Obtener detalle [GET]

+ Response 200 (application/json)

  + Body

    ```
      {
        "raw": {
          "id": 1,
          "id_user": 4,
          "id_test": "test3129",
          "created_at": "2016-06-27T19:07:13+0200"
        },
        "tests": {
          "id_test": "test3129",
          "name": "prueba",
          "instructions": "hola",
          "duration": 5,
          "extra_time": 5,
          "id_user": {
            "id": 4,
            "company_id": {
              "id": 1,
              "name": "Company For Test",
              "created_at": "2016-04-11T22:03:21+0200"
            },
            "rol_id": {
              "id": 1,
              "name": "Manager",
              "created_at": "2016-04-11T22:03:21+0200"
            },
            "name": "Postman 22",
            "lastname": "Chrome 22",
            "email": "pchrome22@gmail.com",
            "password": "$2y$10$HHU.Kp1Rr5UUiRtCdandhOEIouruSqbACfuE267xxsK4uc/MniQxS",
            "is_active": true,
            "created_at": "2016-06-10T12:52:45+0200"
          },
          "is_active": true,
          "is_autocorrect": false,
          "created_at": "2016-06-24T19:27:32+0200"
        }
      }
    ```

# Corregir Examen [/reviewertests/id]

## Modificar [PUT]

+ Request (application/json)

  + Body

    ```
      {
        "id": 5,
        "id_test": "test18707",
        "id_reviewer": 5
      }
    ```

+ Response 200 (application/json)

  + Body

    ```
      {
        "code": 200,
        "message": "OK"
      }
    ```
# Corregir Examen [/reviewertests/id]

## Eliminar [DELETE]

+ Response 200 (application/json)

  + Body

    ```
      {
        "code": 200,
        "message": "OK"
      }
    ```

# Group Candidato

# Candidatos [/candidates]

## Crear nuevo [POST]

+ Request (application/json)

  + Body

    ```
      {
        "id_user": 4,
        "id_test": "test10318",
        "emails": [
          {"email" : "email1@email.com" },
          {"email" : "email2@email.com" },
          {"email" : "email3@email.com" },
          {"email" : "email4@email.com" }
        ]
      }
    ```

+ Response 200 (application/json)

  + Body

    ```
      {
        "code": 200,
        "message": "OK"
      }
    ```

# Candidatos [/candidates]

## Obtener todos [GET]

+ Response 200 (application/json)

  + Body

    ```
       [
        {
          "id": 14,
          "company_id": 1,
          "email": "daniel.rodriguez.d@gmail.com",
          "username": "1426936289",
          "password": "$2y$10$Jn4XqKKYS/00HeBOZQKwBe.0xB.UF0UizdOkUJUJSRdRaipbpTlK2",
          "is_active": true,
          "created_at": "2016-07-02T20:38:48+0200"
        }
      ]
    ```

# Candidatos [/candidates/id]

## Obtener detalle [GET]

+ Response 200 (application/json)

  + Body

    ```
      {
        "id": 14,
        "company_id": 1,
        "email": "daniel.rodriguez.d@gmail.com",
        "username": "1426936289",
        "password": "$2y$10$Jn4XqKKYS/00HeBOZQKwBe.0xB.UF0UizdOkUJUJSRdRaipbpTlK2",
        "is_active": true,
        "created_at": "2016-07-02T20:38:48+0200"
      }
    ```

# Candidatos [/candidates/id]

## Modificar [PUT]

+ Request (application/json)

  + Body

    ```
      {
        "id": 14,
        "company_id": 1,
        "email": "daniel.rodriguez.d@gmail.com",
        "username": "1426936289",
        "password": "$2y$10$Jn4XqKKYS/00HeBOZQKwBe.0xB.UF0UizdOkUJUJSRdRaipbpTlK2",
        "is_active": true,
        "created_at": "2016-07-02T20:38:48+0200"
      }
    ```

+ Response 200 (application/json)

  + Body

    ```
      {
        "code": 200,
        "message": "OK"
      }
    ```
# Candidatos [/candidates/id]

## Eliminar [DELETE]

+ Response 200 (application/json)

  + Body

    ```
      {
        "code": 200,
        "message": "OK"
      }
    ```

# Group Candidato asociado a examen

# Candidatos asociados a examen [/candidatetests]

## Crear nuevo [POST]

+ Request (application/json)

  + Body

    ```
      {
        "id_test" : "test4940",
        "id_candidate" : 3
      }
    ```

+ Response 200 (application/json)

  + Body

    ```
      {
        "code": 200,
        "message": "OK"
      }
    ```

# Candidatos asociados a examen [/candidatetests]

## Obtener todos [GET]

+ Response 200 (application/json)

  + Body

    ```
      {
        "raw": [
          {
            "id": 43,
            "id_test": "test29215",
            "id_candidate": 14,
            "score": 0,
            "started": "2016-07-02T20:39:52+0200",
            "submitted": "2016-07-02T20:40:10+0200",
            "is_taken": true,
            "created_at": "2016-07-02T20:38:48+0200"
          }
        ],
        "tests": [
          {
            "id_test": "test29215",
            "name": "Examen MPWAR",
            "instructions": "Lea las instrucciones de cada pregunta con cuidado y luego compruebe si las ha entendido correctamente. Cualquier error cometido al marcar su respuesta haran que se le califique como incorrecta.",
            "duration": 60,
            "extra_time": 10,
            "id_user": {
              "id": 7,
              "company_id": {
                "id": 1,
                "name": "Company For Test",
                "created_at": "2016-04-11T22:03:21+0200"
              },
              "rol_id": {
                "id": 1,
                "name": "Manager",
                "created_at": "2016-04-11T22:03:21+0200"
              },
              "name": "Andreina ",
              "lastname": "Loriente",
              "email": "andreina.loriente@gmail.com",
              "password": "$2y$10$38rTwbIRnvFoROck5RUG8OKhuUDgZ/N9mVE56lTKSyqAhX8Q5Pi4m",
              "is_active": true,
              "created_at": "2016-06-29T19:25:20+0200"
            },
            "is_active": true,
            "is_autocorrect": true,
            "created_at": "2016-07-02T17:24:46+0200"
          }
        ],
        "candidates": [
          {
            "id": 14,
            "company_id": 1,
            "email": "daniel.rodriguez.d@gmail.com",
            "username": "1426936289",
            "password": "$2y$10$Jn4XqKKYS/00HeBOZQKwBe.0xB.UF0UizdOkUJUJSRdRaipbpTlK2",
            "is_active": true,
            "created_at": "2016-07-02T20:38:48+0200"
          }
        ]
      }
    ```

# Candidatos asociados a examen [/candidatetests/id]

## Obtener detalle [GET]

+ Response 200 (application/json)

  + Body

    ```
      {
        "raw": {
          "id": 43,
          "id_test": "test29215",
          "id_candidate": 14,
          "score": 0,
          "started": "2016-07-02T20:39:52+0200",
          "submitted": "2016-07-02T20:40:10+0200",
          "is_taken": true,
          "created_at": "2016-07-02T20:38:48+0200"
        },
        "tests": {
          "id_test": "test29215",
          "name": "Examen MPWAR",
          "instructions": "Lea las instrucciones de cada pregunta con cuidado y luego compruebe si las ha entendido correctamente. Cualquier error cometido al marcar su respuesta haran que se le califique como incorrecta.",
          "duration": 60,
          "extra_time": 10,
          "id_user": {
            "id": 7,
            "company_id": {
              "id": 1,
              "name": "Company For Test",
              "created_at": "2016-04-11T22:03:21+0200"
            },
            "rol_id": {
              "id": 1,
              "name": "Manager",
              "created_at": "2016-04-11T22:03:21+0200"
            },
            "name": "Andreina ",
            "lastname": "Loriente",
            "email": "andreina.loriente@gmail.com",
            "password": "$2y$10$38rTwbIRnvFoROck5RUG8OKhuUDgZ/N9mVE56lTKSyqAhX8Q5Pi4m",
            "is_active": true,
            "created_at": "2016-06-29T19:25:20+0200"
          },
          "is_active": true,
          "is_autocorrect": true,
          "created_at": "2016-07-02T17:24:46+0200"
        },
        "candidates": {
          "id": 14,
          "company_id": 1,
          "email": "daniel.rodriguez.d@gmail.com",
          "username": "1426936289",
          "password": "$2y$10$Jn4XqKKYS/00HeBOZQKwBe.0xB.UF0UizdOkUJUJSRdRaipbpTlK2",
          "is_active": true,
          "created_at": "2016-07-02T20:38:48+0200"
        }
      }
    ```

# Candidatos asociados a examen [/candidatetests/id]

## Modificar [PUT]

+ Request (application/json)

  + Body

    ```
      {
        "id": 3,
        "id_test": "test4940",
        "id_candidate": 3
      }
    ```

+ Response 200 (application/json)

  + Body

    ```
      {
        "code": 200,
        "message": "OK"
      }
    ```
# Candidatos asociados a examen [/candidatetests/id]

## Eliminar [DELETE]

+ Response 200 (application/json)

  + Body

    ```
      {
        "code": 200,
        "message": "OK"
      }
    ```

# Group Respuestas del candidato

# Resultados de usuario [/candidate_question_answer]

## Crear nuevo [POST]

+ Request (application/json)

  + Body

    ```
      [
        {
            "candidate_id": 1,
            "proposedAnswer_id": 102,
            "answer": "respuesta",
            "file": "",
            "score": 15
        }
      ]
    ```

+ Response 200 (application/json)

  + Body

    ```
      {
        "code": 200,
        "message": "OK"
      }
    ```

# Resultados de usuario [/candidate_question_answer]

## Obtener todos [GET]

+ Response 200 (application/json)

  + Body

    ```
      [
        {
          "id": 40,
          "id_candidate": {
            "id": 14,
            "company_id": 1,
            "email": "daniel.rodriguez.d@gmail.com",
            "username": "1426936289",
            "password": "$2y$10$Jn4XqKKYS/00HeBOZQKwBe.0xB.UF0UizdOkUJUJSRdRaipbpTlK2",
            "is_active": true,
            "created_at": "2016-07-02T20:38:48+0200"
          },
          "id_proposed_answer": {
            "id": 153,
            "question": {
              "id": 59,
              "type": {
                "id": 1,
                "description": "seleccion simple",
                "autocorrect": true,
                "registration_date": "2015-08-25T22:47:19+0200"
              },
              "id_test": "test29215",
              "description": "Que significado tienen las siglas MPWAR",
              "score": 10,
              "created_at": "2016-07-02T17:29:40+0200"
            },
            "answer": "Máster en Programación Web de Alto Rendimiento",
            "is_correct": true,
            "score": 10,
            "file": "Resource id #422",
            "created_at": "2016-07-02T17:29:42+0200"
          },
          "answer": "Máster en Programación Web de Alto Rendimiento",
          "file": "Resource id #321",
          "score": 10,
          "created_at": "2016-07-02T20:40:12+0200"
        }
      ]
    ```

# Resultados de usuario [/candidate_question_answer/id]

## Obtener detalle [GET]

+ Response 200 (application/json)

  + Body

    ```
      {
        "id": 40,
        "id_candidate": {
          "id": 14,
          "company_id": 1,
          "email": "daniel.rodriguez.d@gmail.com",
          "username": "1426936289",
          "password": "$2y$10$Jn4XqKKYS/00HeBOZQKwBe.0xB.UF0UizdOkUJUJSRdRaipbpTlK2",
          "is_active": true,
          "created_at": "2016-07-02T20:38:48+0200"
        },
        "id_proposed_answer": {
          "id": 153,
          "question": {
            "id": 59,
            "type": {
              "id": 1,
              "description": "seleccion simple",
              "autocorrect": true,
              "registration_date": "2015-08-25T22:47:19+0200"
            },
            "id_test": "test29215",
            "description": "Que significado tienen las siglas MPWAR",
            "score": 10,
            "created_at": "2016-07-02T17:29:40+0200"
          },
          "answer": "Máster en Programación Web de Alto Rendimiento",
          "is_correct": true,
          "score": 10,
          "file": "Resource id #422",
          "created_at": "2016-07-02T17:29:42+0200"
        },
        "answer": "Máster en Programación Web de Alto Rendimiento",
        "file": "Resource id #321",
        "score": 10,
        "created_at": "2016-07-02T20:40:12+0200"
      }
    ```

# Resultados de usuario [/candidate_question_answer/id]

## Modificar [PUT]

+ Request (application/json)

  + Body

    ```
      [
        {
          "id": 5,
          "candidate_id": 1,
          "proposedAnswer_id": 102,
          "answer": "respuesta",
          "file": "",
          "score": 15
        }
      ]
    ```

+ Response 200 (application/json)

  + Body

    ```
      {
        "code": 200,
        "message": "OK"
      }
    ```

# Resultados de usuario [/candidate_question_answer/id]

## Eliminar [DELETE]

+ Response 200 (application/json)

  + Body

    ```
      {
        "code": 200,
        "message": "OK"
      }
    ```

# Group Rol

# Rol [/rol]

## Crear nuevo [POST]

+ Request (application/json)

  + Body

    ```
      {
        "name" : "Nuevo rol"
      }
    ```

+ Response 200 (application/json)

  + Body

    ```
      {
        "code": 200,
        "message": "OK"
      }
    ```

# Rol [/rol]

## Obtener todos [GET]

+ Response 200 (application/json)

  + Body

    ```
      [
        {
          "id": 1,
          "name": "Manager",
          "created_at": "2016-04-11T22:03:21+0200"
        },
        {
          "id": 2,
          "name": "Reviewer",
          "created_at": "2016-04-11T22:03:21+0200"
        }
      ]
    ```

# Rol [/rol/id]

## Obtener detalle [GET]

+ Response 200 (application/json)

  + Body

    ```
      {
        "id": 1,
        "name": "Manager",
        "created_at": "2016-04-11T22:03:21+0200"
      }
    ```

# Rol [/rol/id]

## Modificar [PUT]

+ Request (application/json)

  + Body

    ```
      {
        "id": 1,
        "name": "Manager"
      }
    ```

+ Response 200 (application/json)

  + Body

    ```
      {
        "code": 200,
        "message": "OK"
      }
    ```

# Rol [/rol/id]

## Eliminar [DELETE]

+ Response 200 (application/json)

  + Body

    ```
      {
        "code": 200,
        "message": "OK"
      }
    ```

# Group Compañia

# Compañia [/company]

## Crear nuevo [POST]

+ Request (application/json)

  + Body

    ```
      {
        "name" : "Nueva compañia"
      }
    ```

+ Response 200 (application/json)

  + Body

    ```
      {
        "code": 200,
        "message": "OK"
      }
    ```

# Compañia [/company]

## Obtener todos [GET]

+ Response 200 (application/json)

  + Body

    ```
      [
        {
          "id": 1,
          "name": "Company For Test",
          "created_at": "2016-04-11T22:03:21+0200"
        }
      ]
    ```

# Compañia [/company/id]

## Obtener detalle [GET]

+ Response 200 (application/json)

  + Body

    ```
      {
        "id": 1,
        "name": "Company For Test",
        "created_at": "2016-04-11T22:03:21+0200"
      }
    ```

# Compañia [/company/id]

## Modificar [PUT]

+ Request (application/json)

  + Body

    ```
      {
        "id": 1,
        "name" : "Nueva compañia"
      }
    ```

+ Response 200 (application/json)

  + Body

    ```
      {
        "code": 200,
        "message": "OK"
      }
    ```

# Compañia [/company/id]

## Eliminar [DELETE]

+ Response 200 (application/json)

  + Body

    ```
      {
        "code": 200,
        "message": "OK"
      }
    ```

# Group Usuario

# Usuario [/user]

## Crear nuevo [POST]

+ Request (application/json)

  + Body

    ```
      {
        "company_id": 2,
        "rol_id": 1,
        "name": "Juan",
        "lastname": "Perez",
        "email": "juanperez@gmail.com",
        "password": "secure password here"
      }
    ```

+ Response 200 (application/json)

  + Body

    ```
      {
        "code": 200,
        "message": "OK"
      }
    ```

# Usuario [/user]

## Obtener todos [GET]

+ Response 200 (application/json)

  + Body

    ```
      [
        {
          "id": 1,
          "company_id": {
            "id": 1,
            "name": "Company For Test",
            "created_at": "2016-04-11T22:03:21+0200"
          },
          "rol_id": {
            "id": 1,
            "name": "Manager",
            "created_at": "2016-04-11T22:03:21+0200"
          },
          "name": "Juan",
          "lastname": "Perez",
          "email": "juanperez@gmail.com",
          "password": "$2y$10$UEgJgPpu8fyWS12VrYQwQ.kzklQpNJ0ITB8cqgcdqL9Vp01hzV.m2",
          "is_active": true,
          "created_at": "2016-04-11T22:03:21+0200"
        }
      ]
    ```

# Usuario [/user/id]

## Obtener detalle [GET]

+ Response 200 (application/json)

  + Body

    ```
      {
        "id": 1,
        "company_id": {
          "id": 1,
          "name": "Company For Test",
          "created_at": "2016-04-11T22:03:21+0200"
        },
        "rol_id": {
          "id": 1,
          "name": "Manager",
          "created_at": "2016-04-11T22:03:21+0200"
        },
        "name": "Juan",
        "lastname": "Perez",
        "email": "juanperez@gmail.com",
        "password": "$2y$10$UEgJgPpu8fyWS12VrYQwQ.kzklQpNJ0ITB8cqgcdqL9Vp01hzV.m2",
        "is_active": true,
        "created_at": "2016-04-11T22:03:21+0200"
      }
    ```

# Usuario [/user/id]

## Modificar [PUT]

+ Request (application/json)

  + Body

    ```
      {
        "id": 1,
        "company_id": 2,
        "rol_id": 1,
        "name": "Juan",
        "lastname": "Perez",
        "email": "juanperez@gmail.com",
        "password": "secure password here"
      }
    ```

+ Response 200 (application/json)

  + Body

    ```
      {
        "code": 200,
        "message": "OK"
      }
    ```

# Usuario [/user/id]

## Eliminar [DELETE]

+ Response 200 (application/json)

  + Body

    ```
      {
        "code": 200,
        "message": "OK"
      }
    ```

# Group Rol por usuario

# Rol por usuario [/rol_permit]

## Obtener todos [GET]

+ Response 200 (application/json)

  + Body

    ```
      [
        {
          "id": 1,
          "id_rol": 1,
          "id_permit": 1
        }
      ]
    ```

# Group Login

# Login Usuario [/user/login]

## Iniciar sesión [POST]

+ Request (application/json)

  + Body

    ```
      {
       "username" : "p@p.com",
       "password" : "password31"
      }
    ```

+ Response 200 (application/json)

  + Body

    ```
      {
        "code": 200,
        "message": {
          "user": {
            "id": 5,
            "company_id": {
              "id": 1,
              "name": "Company For Test",
              "created_at": "2016-04-11T22:03:21+0200"
            },
            "rol_id": {
              "id": 2,
              "name": "Reviewer",
              "created_at": "2016-04-11T22:03:21+0200"
            },
            "name": "prueba",
            "lastname": "prueba",
            "email": "p@p.com",
            "password": "$2y$10$WEaNkeBIX./qldoL8/zU7OCl6YflcKhi7U/MG5SDkZlvDf82huQei",
            "is_active": true,
            "created_at": "2016-06-26T13:39:44+0200"
          },
          "key": "eyJ0eXAiOiJKV1QiLCJhbGciOiJub25lIiwianRpIjoiNSJ9.eyJpc3MiOiJodHRwOlwvXC9wb3J0YWwuZGV2IiwiYXVkIjoiaHR0cDpcL1wvcG9ydGFsLm9yZ1wvIiwianRpIjoiNSIsImlhdCI6MTQ2NzU0MTUwNSwibmJmIjoxNDY3NTQxNTA2LCJleHAiOjE0Njc2Mjc5MDUsInVpZCI6IjFkNThkOTQ3YjU2NjJkMGIifQ.c270342794f57937f3b83b10d2e1d4747573b135ea2e56f44122024cf355b6b2"
        }
      }
    ```

# Login Candidato [/candidato/login]

## Iniciar sesión [POST]

+ Request (application/json)

  + Body

    ```
      {
       "username" : "0660332788",
       "password" : "w9wHi8edFv"
      }
    ```

+ Response 200 (application/json)

  + Body

    ```
      {
        "code": 200,
        "message": {
            "user": {
                "id": 15,
                "company_id": 1,
                "email": "ninina31@gmail.com",
                "username": "0660332788",
                "password": "$2y$10$LD5B.o6c3L4bopcXomnp4uR87npq8qZeaScFbmw0UbWxq6efBGMQ.",
                "is_active": true,
                "created_at": "2016-07-02T20:38:51+0200"
            },
            "key": "eyJ0eXAiOiJKV1QiLCJhbGciOiJub25lIiwianRpIjoiMTUifQ.eyJpc3MiOiJodHRwOlwvXC9wb3J0YWwuZGV2IiwiYXVkIjoiaHR0cDpcL1wvcG9ydGFsLm9yZ1wvIiwianRpIjoiMTUiLCJpYXQiOjE0Njc1NDIxMTUsIm5iZiI6MTQ2NzU0MjExNiwiZXhwIjoxNDY3NjI4NTE1LCJ1aWQiOiIzYTI4YmZmOTI2ZDBmODY1In0.9b8e4898ecfd41825f797617b5c2bcfd4a7fcb2436e090bab63489becb2adac4"
        }
    }
    ```
