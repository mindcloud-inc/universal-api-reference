# CardClan: Get Integration Configuration

Retrieves a CardClan integration configuration by ID.

```
GET https://connect.mindcloud.co/v1/universal/cardClan/latest/actions/get-integration-configuration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CardClan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cardClan/latest/actions/get-integration-configuration?connectionId=$CONNECTION_ID&integrationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "integrationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cardClan/latest/actions/get-integration-configuration?${params}`, {
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
| `integrationId` | string | yes | Integration configuration ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "card": {},
      "emailAccount": [
        {}
      ],
      "key": "string",
      "mergeTags": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `card` | object | Configured card summary. |
| `emailAccount` | array<object> | Configured sender email accounts for the integration. |
| `key` | string | Top-level response group key. |
| `mergeTags` | array<object> | Configured merge-tag definitions. |

## Native endpoint

Through the native CardClan API, this operation is `GET /integration/config` (base URL `https://app.cardclan.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-integration-configuration.md) for the provider-specific parameters and requirements.

