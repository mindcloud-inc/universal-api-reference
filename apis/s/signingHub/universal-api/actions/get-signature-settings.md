# SigningHub: Get Signature Settings

Retrieves signature settings from SigningHub.

```
GET https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/get-signature-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SigningHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/get-signature-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/get-signature-settings?${params}`, {
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
      "level_of_assurance": {},
      "signature": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `level_of_assurance` | object |  |
| `signature` | object |  |

## Native endpoint

Through the native SigningHub API, this operation is `GET /v4/settings/signatures` (base URL `https://api.signinghub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-signature-settings.md) for the provider-specific parameters and requirements.

