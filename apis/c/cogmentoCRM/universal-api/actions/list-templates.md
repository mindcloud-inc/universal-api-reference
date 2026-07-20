# Cogmento CRM: List Templates



```
GET https://connect.mindcloud.co/v1/universal/cogmentoCRM/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cogmento CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cogmentoCRM/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cogmentoCRM/latest/actions/list-templates?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "call": {
        "default": "string",
        "templates": {},
        "total": 1
      },
      "case": {
        "default": "string",
        "templates": {},
        "total": 1
      },
      "company": {
        "default": "string",
        "templates": {},
        "total": 1
      },
      "contact": {
        "default": "string",
        "templates": {},
        "total": 1
      },
      "custom": {},
      "deal": {
        "default": "string",
        "templates": {},
        "total": 1
      },
      "document": {
        "default": "string",
        "templates": {},
        "total": 1
      },
      "event": {
        "default": "string",
        "templates": {},
        "total": 1
      },
      "product": {
        "default": "string",
        "templates": {},
        "total": 1
      },
      "task": {
        "default": "string",
        "templates": {},
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `call.default` | string |  |
| `call.templates` | object |  |
| `call.total` | number |  |
| `case.default` | string |  |
| `case.templates` | object |  |
| `case.total` | number |  |
| `company.default` | string |  |
| `company.templates` | object |  |
| `company.total` | number |  |
| `contact.default` | string |  |
| `contact.templates` | object |  |
| `contact.total` | number |  |
| `custom` | object |  |
| `deal.default` | string |  |
| `deal.templates` | object |  |
| `deal.total` | number |  |
| `document.default` | string |  |
| `document.templates` | object |  |
| `document.total` | number |  |
| `event.default` | string |  |
| `event.templates` | object |  |
| `event.total` | number |  |
| `product.default` | string |  |
| `product.templates` | object |  |
| `product.total` | number |  |
| `task.default` | string |  |
| `task.templates` | object |  |
| `task.total` | number |  |

## Native endpoint

Through the native Cogmento CRM API, this operation is `GET /templates/` (base URL `https://api.freecrm.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

