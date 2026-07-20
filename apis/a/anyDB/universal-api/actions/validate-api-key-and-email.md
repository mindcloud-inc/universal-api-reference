# AnyDB: Validate API Key And Email

Validates API key and email in AnyDB.

```
GET https://connect.mindcloud.co/v1/universal/anyDB/latest/actions/validate-api-key-and-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AnyDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anyDB/latest/actions/validate-api-key-and-email?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/anyDB/latest/actions/validate-api-key-and-email?${params}`, {
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
      "email": "ava@example.com",
      "reason": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | The authenticated AnyDB email address echoed by the provider. |
| `reason` | string | Provider-supplied error reason when authentication fails. |
| `success` | boolean | Whether the AnyDB credentials are valid. |

## Native endpoint

Through the native AnyDB API, this operation is `POST /api/integrations/ext/checkauth` (base URL `https://app.anydb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-api-key-and-email.md) for the provider-specific parameters and requirements.

