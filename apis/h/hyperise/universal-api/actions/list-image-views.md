# Hyperise: List Image Views

Retrieves image views for an image template in Hyperise.

```
GET https://connect.mindcloud.co/v1/universal/hyperise/latest/actions/list-image-views
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hyperise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hyperise/latest/actions/list-image-views?connectionId=$CONNECTION_ID&imageHash=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "imageHash": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hyperise/latest/actions/list-image-views?${params}`, {
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
| `dateFrom` | string | no | Optional ISO timestamp to fetch impressions since a specific time. |
| `imageHash` | string | yes | The Hyperise image template hash to fetch impressions for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "businessName": "Ava Chen",
          "enrichmentData": {
            "businessName": "Ava Chen",
            "email": "ava@example.com",
            "firstName": "Ava",
            "lastName": "Chen"
          },
          "id": 1,
          "imageName": "Ava Chen",
          "imageUrl": "https://example.com",
          "processedAt": "string"
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
| `data[].businessName` | string |  |
| `data[].enrichmentData.businessName` | string |  |
| `data[].enrichmentData.email` | string |  |
| `data[].enrichmentData.firstName` | string |  |
| `data[].enrichmentData.lastName` | string |  |
| `data[].id` | number |  |
| `data[].imageName` | string |  |
| `data[].imageUrl` | string |  |
| `data[].processedAt` | string |  |

## Native endpoint

Through the native Hyperise API, this operation is `GET /image-impressions` (base URL `https://app.hyperise.io/api/v1/regular`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-image-views.md) for the provider-specific parameters and requirements.

