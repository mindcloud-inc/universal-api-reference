# profileAPI: Lookup Phone

Finds a phone contact in profileAPI by person details.

```
GET https://connect.mindcloud.co/v1/universal/profileAPI/latest/actions/lookup-phone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a profileAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/profileAPI/latest/actions/lookup-phone?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/profileAPI/latest/actions/lookup-phone?${params}`, {
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
| `id` | string | no | Person UUID option for phone lookup. Example: `9e6a55b258ef11edb8780242ac120002`. |
| `firstName` | string | no | First-name field for name plus website phone lookup. Example: `Joe`. |
| `lastName` | string | no | Last-name field for name plus website phone lookup. Example: `Doe`. |
| `website` | string | no | Company website for name plus website phone lookup. Example: `https://acme.com`. |
| `linkedInUrl` | string | no | LinkedIn profile URL lookup option. Example: `https://linkedin.com/in/joedoe`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "lastValidatedAt": "2026-05-07T12:00:00.000Z",
      "phone": "string",
      "scoreValue": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `lastValidatedAt` | date |  |
| `phone` | string |  |
| `scoreValue` | number |  |
| `type` | string |  |

## Native endpoint

Through the native profileAPI API, this operation is `POST /phone-contacts/lookup` (base URL `https://api.profileapi.com/2024-03-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-phone.md) for the provider-specific parameters and requirements.

