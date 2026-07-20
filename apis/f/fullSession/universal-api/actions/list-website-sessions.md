# FullSession: List Website Sessions

Retrieves website visitor sessions from FullSession.

```
GET https://connect.mindcloud.co/v1/universal/fullSession/latest/actions/list-website-sessions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FullSession `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fullSession/latest/actions/list-website-sessions?connectionId=$CONNECTION_ID&customerId=string&siteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "string",
  "siteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fullSession/latest/actions/list-website-sessions?${params}`, {
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
| `customerId` | string | yes | Unique customer ID from Fullsession Setup. |
| `siteId` | string | yes | Unique site ID for the selected domain. |
| `startAfter` | number | no | Optional session timestamp in milliseconds. When provided, use the returned startAfter value to continue pagination. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activeTime": 1,
      "browser": "string",
      "browserFullVersion": "string",
      "city": "string",
      "country": "string",
      "countryCode": "string",
      "device": "string",
      "duration": 1,
      "endTime": 1,
      "exitPage": "string",
      "landingPage": "string",
      "os": "string",
      "pages": [
        {
          "fullPath": "string"
        }
      ],
      "referrer": "string",
      "startTime": 1,
      "userId": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeTime` | number |  |
| `browser` | string |  |
| `browserFullVersion` | string |  |
| `city` | string |  |
| `country` | string |  |
| `countryCode` | string |  |
| `device` | string |  |
| `duration` | number |  |
| `endTime` | number |  |
| `exitPage` | string |  |
| `landingPage` | string |  |
| `os` | string |  |
| `pages[].fullPath` | string |  |
| `referrer` | string |  |
| `startTime` | number |  |
| `userId` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native FullSession API, this operation is `GET /sessions/:customerId/:siteId` (base URL `https://app.fullsession.io/v1/external`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-website-sessions.md) for the provider-specific parameters and requirements.

