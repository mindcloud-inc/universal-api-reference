# Anabix CRM: Get Activity

Retrieves an activity from Anabix CRM.

```
GET https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/get-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anabix CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/get-activity?connectionId=$CONNECTION_ID&data.idActivity=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "data.idActivity": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/get-activity?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data.idActivity` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": "string",
      "customFields": [
        {}
      ],
      "duration": "string",
      "idActivity": 1,
      "idContact": 1,
      "idDeal": 1,
      "revisionInfo": {},
      "timestamp": 1,
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string |  |
| `customFields` | array<object> |  |
| `duration` | string |  |
| `idActivity` | number | Anabix activity ID. |
| `idContact` | number |  |
| `idDeal` | number |  |
| `revisionInfo` | object |  |
| `timestamp` | number |  |
| `title` | string | Activity title. |
| `type` | string |  |

## Native endpoint

Through the native Anabix CRM API, this operation is `POST /api` (base URL `https://app.anabix.cz`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-activity.md) for the provider-specific parameters and requirements.

