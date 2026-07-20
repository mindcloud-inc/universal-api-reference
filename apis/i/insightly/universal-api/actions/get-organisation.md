# Insightly: Get Organisation

Retrieves an organisation from Insightly by ID.

```
GET https://connect.mindcloud.co/v1/universal/insightly/latest/actions/get-organisation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insightly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insightly/latest/actions/get-organisation?connectionId=$CONNECTION_ID&organisationId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organisationId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/insightly/latest/actions/get-organisation?${params}`, {
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
| `organisationId` | number | yes | The Organisation ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "background": "string",
      "createdUserId": 1,
      "dateCreatedUtc": "2026-05-07T12:00:00.000Z",
      "dateUpdatedUtc": "2026-05-07T12:00:00.000Z",
      "imageUrl": "https://example.com",
      "lastActivityDateUtc": "2026-05-07T12:00:00.000Z",
      "nextActivityDateUtc": "2026-05-07T12:00:00.000Z",
      "organisationId": 1,
      "organisationName": "Ava Chen",
      "ownerUserId": 1,
      "phone": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `background` | string |  |
| `createdUserId` | number |  |
| `dateCreatedUtc` | date |  |
| `dateUpdatedUtc` | date |  |
| `imageUrl` | string |  |
| `lastActivityDateUtc` | date |  |
| `nextActivityDateUtc` | date |  |
| `organisationId` | number |  |
| `organisationName` | string |  |
| `ownerUserId` | number |  |
| `phone` | string |  |
| `website` | string |  |

## Native endpoint

Through the native Insightly API, this operation is `GET {{credentials.apiBaseUrl}}Organisations/:organisationId` (base URL `https://api.na1.insightly.com/v3.1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organisation.md) for the provider-specific parameters and requirements.

