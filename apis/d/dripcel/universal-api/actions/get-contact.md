# Dripcel: Get Contact

Retrieves a contact from Dripcel by cell number.

```
GET https://connect.mindcloud.co/v1/universal/dripcel/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dripcel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dripcel/latest/actions/get-contact?connectionId=$CONNECTION_ID&cell=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cell": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dripcel/latest/actions/get-contact?${params}`, {
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
| `cell` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "cell": "string",
        "country": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "dedupedCampaignIds": [
          "string"
        ],
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "ok": true,
      "requestId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.cell` | string |  |
| `data.country` | string |  |
| `data.createdAt` | date |  |
| `data.dedupedCampaignIds[]` | string |  |
| `data.updatedAt` | date |  |
| `ok` | boolean |  |
| `requestId` | string |  |

## Native endpoint

Through the native Dripcel API, this operation is `GET /contacts/:cell` (base URL `https://api.dripcel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

