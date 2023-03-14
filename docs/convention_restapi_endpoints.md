# [Your API endpoint name]

Explain briefly what thing make the endpoint

**URL** : `/your/path/`

**Method** : `POST|GET|PUT|DELETE|PATCH`

**Auth required** : YES/NO

**Permissions required** : None/Add permissions

**Data constraints**

- list all constrains of data body

```json
{
    "name": "[unicode 64 chars max]"
}
```

**Data example** All fields must be sent.

```json
{
    "name": "Build something project dot com"
}
```

## Success Response

**Condition** : If everything is OK and other conditions

**Code** : `201 CREATED/ other codes`

**Content example**

```json
{
    "id": 123,
    "name": "Build something project dot com"
}
```

## Error Responses

**Condition** : If Account already, some action

**Code** : `303 SEE OTHER`

**Headers** : `Location: http://testserver/api/accounts/123/`

**Content** : `{}`

### Or

**Condition** : If fields are missed.

**Code** : `400 BAD REQUEST`

**Content example**

```json
{
    "name": [
        "This field is required."
    ]
}
```

## Notes

- Add some hints regarding external things can affect your endpoint call