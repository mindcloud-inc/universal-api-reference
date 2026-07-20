# smsmode: List Credentials



```
GET https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/list-credentials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a smsmode `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/list-credentials?connectionId=$CONNECTION_ID&limit=25&offset=0&channelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "channelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/list-credentials?${params}`, {
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
| `channelId` | string | yes | Channel ID path parameter from the smsmode API route. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archivePeriod": 1,
      "authorizedIps": [
        "string"
      ],
      "blocked": true,
      "channel": {
        "channelId": "string",
        "flow": "string",
        "name": "Ava Chen",
        "organisationId": "string",
        "type": "string"
      },
      "creationDate": "2026-05-07T12:00:00.000Z",
      "credentialId": "string",
      "email": "ava@example.com",
      "href": "string",
      "lastIpAddress": "string",
      "lastPasswordUpdateDate": "2026-05-07T12:00:00.000Z",
      "lastUseDate": "2026-05-07T12:00:00.000Z",
      "modificationDate": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "roles": [
        "string"
      ],
      "state": "string",
      "twoFaEnabled": true,
      "twoFaType": "string",
      "type": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archivePeriod` | number |  |
| `authorizedIps[]` | string |  |
| `blocked` | boolean |  |
| `channel.channelId` | string |  |
| `channel.flow` | string |  |
| `channel.name` | string |  |
| `channel.organisationId` | string |  |
| `channel.type` | string |  |
| `creationDate` | date |  |
| `credentialId` | string |  |
| `email` | string |  |
| `href` | string |  |
| `lastIpAddress` | string |  |
| `lastPasswordUpdateDate` | date |  |
| `lastUseDate` | date |  |
| `modificationDate` | date |  |
| `name` | string |  |
| `roles[]` | string |  |
| `state` | string |  |
| `twoFaEnabled` | boolean |  |
| `twoFaType` | string |  |
| `type` | string |  |
| `value` | string |  |

## Native endpoint

Through the native smsmode API, this operation is `GET commons/v1/channels/:channelId/credentials` (base URL `https://rest.smsmode.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-credentials.md) for the provider-specific parameters and requirements.

