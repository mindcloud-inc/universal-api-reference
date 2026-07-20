# Sessionize: List Speaker Wall

Retrieves speaker wall profiles from Sessionize.

```
GET https://connect.mindcloud.co/v1/universal/sessionize/latest/actions/list-speaker-wall
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sessionize `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sessionize/latest/actions/list-speaker-wall?connectionId=$CONNECTION_ID&endpointId=jl4ktls0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "endpointId": "jl4ktls0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sessionize/latest/actions/list-speaker-wall?${params}`, {
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
| `endpointId` | string | yes | Sessionize event API endpoint ID from URLs like https://sessionize.com/api/v2/{endpointId}/view/SpeakerWall. Default: `jl4ktls0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "id": "string",
      "isTopSpeaker": true,
      "lastName": "Chen",
      "profilePicture": "https://example.com",
      "tagLine": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `firstName` | string | Speaker first name. |
| `fullName` | string | Speaker full name. |
| `id` | string | Speaker identifier. |
| `isTopSpeaker` | boolean | Whether the speaker is marked as top speaker. |
| `lastName` | string | Speaker last name. |
| `profilePicture` | string | Speaker profile image URL. |
| `tagLine` | string | Speaker tagline. |

## Native endpoint

Through the native Sessionize API, this operation is `GET /api/v2/:endpointId/view/SpeakerWall` (base URL `https://sessionize.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-speaker-wall.md) for the provider-specific parameters and requirements.

