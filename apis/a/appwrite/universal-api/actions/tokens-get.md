# Appwrite: Get token

Retrieves token details from your Appwrite project.

```
GET https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tokens-get
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tokens-get?connectionId=$CONNECTION_ID&tokenId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tokenId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tokens-get?${params}`, {
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
| `tokenId` | string | yes | Token ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$createdAt": "string",
      "$id": "string",
      "accessedAt": "string",
      "expire": "string",
      "resourceId": "string",
      "resourceType": "string",
      "secret": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$createdAt` | string | Token creation date in ISO 8601 format. |
| `$id` | string | Token ID. |
| `accessedAt` | string | Most recent access date in ISO 8601 format. This attribute is only updated again after 24 hours. |
| `expire` | string | Token expiration date in ISO 8601 format. |
| `resourceId` | string | Resource ID. |
| `resourceType` | string | Resource type. |
| `secret` | string | JWT encoded string. |

## Native endpoint

Through the native Appwrite API, this operation is `GET /tokens/{tokenId}` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/tokens-get.md) for the provider-specific parameters and requirements.

