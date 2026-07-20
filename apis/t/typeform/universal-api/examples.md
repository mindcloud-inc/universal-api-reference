# Typeform Universal API Examples

These examples use the MindCloud API key and Typeform connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User Details



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typeform/latest/actions/get-current-user-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typeform/latest/actions/get-current-user-details?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "alias": "string",
      "email": "ava@example.com",
      "language": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User Details action reference](actions/get-current-user-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/typeform/latest/actions/get-current-user-details).

## Auto-Translate Form



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/typeform/latest/actions/auto-translate-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string",
  "language": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/typeform/latest/actions/auto-translate-form', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string",
    "language": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "fields": [
        {
          "attachment": {
            "properties": {
              "description": "string"
            }
          },
          "id": "string",
          "layout": {
            "attachment": {
              "properties": {
                "description": "string"
              }
            }
          },
          "properties": {
            "buttonText": "string",
            "choices": [
              {
                "attachment": {
                  "properties": {
                    "description": "string"
                  }
                },
                "id": "string",
                "label": "string"
              }
            ],
            "description": "string",
            "labels": {
              "center": "string",
              "left": "string",
              "right": "string"
            }
          },
          "title": "string"
        }
      ],
      "messages": {
        "block": {
          "dropdownPlaceholder": "string",
          "longtextHint": "string",
          "shortTextPlaceholder": "string"
        },
        "label": {
          "buttonOk": "string",
          "buttonSubmit": "string",
          "errorRequired": "string",
          "warningConnection": "string"
        }
      },
      "thankyouScreens": [
        {
          "attachment": {
            "properties": {
              "description": "string"
            }
          },
          "id": "string",
          "layout": {
            "attachment": {
              "properties": {
                "description": "string"
              }
            }
          },
          "properties": {
            "buttonText": "string",
            "description": "string"
          },
          "title": "string"
        }
      ],
      "welcomeScreens": [
        {
          "attachment": {
            "properties": {
              "description": "string"
            }
          },
          "id": "string",
          "layout": {
            "attachment": {
              "properties": {
                "description": "string"
              }
            }
          },
          "properties": {
            "buttonText": "string",
            "description": "string"
          },
          "title": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Auto-Translate Form action reference](actions/auto-translate-form.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/typeform/latest/actions/auto-translate-form).
