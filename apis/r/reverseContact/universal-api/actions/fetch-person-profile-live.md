# Reverse Contact: Fetch Person Profile Live



```
GET https://connect.mindcloud.co/v1/universal/reverseContact/latest/actions/fetch-person-profile-live
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reverse Contact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reverseContact/latest/actions/fetch-person-profile-live?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reverseContact/latest/actions/fetch-person-profile-live?${params}`, {
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
| `url` | string | yes | Public Social profile URL to fetch live. |
| `webhookUrl` | string | no | HTTPS callback URL for live results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "backgroundUrl": "https://example.com",
      "connectionsCount": 1,
      "creationDate": "2026-05-07T12:00:00.000Z",
      "currentPosition": {
        "companyLogoUrl": "https://example.com",
        "companyName": "Ava Chen",
        "companyUrl": "https://example.com",
        "title": "string"
      },
      "experience": [
        {
          "companyLinkedinId": "https://example.com",
          "companyLogoUrl": "https://example.com",
          "companyName": "Ava Chen",
          "companyUrl": "https://example.com",
          "contractType": "string",
          "description": "string",
          "startEndDate": {
            "end": "2026-05-07T12:00:00.000Z",
            "start": "2026-05-07T12:00:00.000Z"
          },
          "title": "string"
        }
      ],
      "firstName": "Ava",
      "followersCount": 1,
      "hasPremium": true,
      "hasVerificationBadge": true,
      "headline": "string",
      "isOpenToWork": true,
      "lastName": "Chen",
      "linkedinUrl": "https://example.com",
      "location": {
        "city": "string",
        "country": "string",
        "countryCode": "string",
        "state": "string"
      },
      "memberId": "string",
      "photoUrl": "https://example.com",
      "pronoun": "string",
      "publicId": "string",
      "summary": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `backgroundUrl` | string |  |
| `connectionsCount` | number |  |
| `creationDate` | date |  |
| `currentPosition.companyLogoUrl` | string |  |
| `currentPosition.companyName` | string |  |
| `currentPosition.companyUrl` | string |  |
| `currentPosition.title` | string |  |
| `experience[].companyLinkedinId` | string |  |
| `experience[].companyLogoUrl` | string |  |
| `experience[].companyName` | string |  |
| `experience[].companyUrl` | string |  |
| `experience[].contractType` | string |  |
| `experience[].description` | string |  |
| `experience[].startEndDate.end` | date |  |
| `experience[].startEndDate.start` | date |  |
| `experience[].title` | string |  |
| `firstName` | string |  |
| `followersCount` | number |  |
| `hasPremium` | boolean |  |
| `hasVerificationBadge` | boolean |  |
| `headline` | string |  |
| `isOpenToWork` | boolean |  |
| `lastName` | string |  |
| `linkedinUrl` | string |  |
| `location.city` | string |  |
| `location.country` | string |  |
| `location.countryCode` | string |  |
| `location.state` | string |  |
| `memberId` | string |  |
| `photoUrl` | string |  |
| `pronoun` | string |  |
| `publicId` | string |  |
| `summary` | string |  |

## Native endpoint

Through the native Reverse Contact API, this operation is `POST /v2/fetch/persons/live` (base URL `https://api.reversecontact.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-person-profile-live.md) for the provider-specific parameters and requirements.

