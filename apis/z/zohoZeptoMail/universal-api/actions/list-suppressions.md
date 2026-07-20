# Zoho ZeptoMail: List Suppressions

Retrieves suppression list entries from Zoho ZeptoMail.

```
GET https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/list-suppressions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho ZeptoMail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/list-suppressions?connectionId=$CONNECTION_ID&type=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "type": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/list-suppressions?${params}`, {
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
| `type` | string | yes | Suppression category to manage. |
| `mailagent_keys[0]` | string | no | Filter suppression entries by agent alias. |
| `limit` | number | no | Maximum number of suppression entries to return. |
| `offset` | number | no | Number of suppression entries to skip before returning results. |
| `dateFrom` | string | no | Fetch entries modified on or after this date and time. |
| `dateTo` | string | no | Fetch entries modified on or before this date and time. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "action": "string",
          "description": "string",
          "mailagent_key": "string",
          "modified_time": "2026-05-07T12:00:00.000Z",
          "status": "string",
          "value": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].action` | string |  |
| `data[].description` | string |  |
| `data[].mailagent_key` | string |  |
| `data[].modified_time` | date |  |
| `data[].status` | string |  |
| `data[].value` | string |  |

## Native endpoint

Through the native Zoho ZeptoMail API, this operation is `GET suppressions/:type` (base URL `https://api.zeptomail.com/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-suppressions.md) for the provider-specific parameters and requirements.

