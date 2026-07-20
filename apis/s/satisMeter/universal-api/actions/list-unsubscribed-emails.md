# SatisMeter: List Unsubscribed Emails



```
GET https://connect.mindcloud.co/v1/universal/satisMeter/latest/actions/list-unsubscribed-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SatisMeter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/satisMeter/latest/actions/list-unsubscribed-emails?connectionId=$CONNECTION_ID&projectId=61fce0adea447e24ec27d606" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "61fce0adea447e24ec27d606"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/satisMeter/latest/actions/list-unsubscribed-emails?${params}`, {
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
| `projectId` | string | yes | Project ID. Example: `61fce0adea447e24ec27d606`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "attributes": {
          "emails": [
            "ava@example.com"
          ]
        },
        "id": "string",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Project unsubscribe resource. |
| `data.attributes` | object | Unsubscribe attributes. |
| `data.attributes.emails` | array<string> | Unsubscribed email addresses. |
| `data.id` | string | Project ID. |
| `data.type` | string | Resource type. |

## Native endpoint

Through the native SatisMeter API, this operation is `GET /api/v2/project-unsubscribes/:projectId` (base URL `https://app.satismeter.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-unsubscribed-emails.md) for the provider-specific parameters and requirements.

