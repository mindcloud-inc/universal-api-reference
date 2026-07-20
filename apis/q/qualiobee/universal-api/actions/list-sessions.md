# Qualiobee: List Sessions

Retrieves sessions from Qualiobee.

```
GET https://connect.mindcloud.co/v1/universal/qualiobee/latest/actions/list-sessions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qualiobee `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qualiobee/latest/actions/list-sessions?connectionId=$CONNECTION_ID&limit=25&offset=0&organizationUuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organizationUuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qualiobee/latest/actions/list-sessions?${params}`, {
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
| `organizationUuid` | string | yes |  |
| `withDeleted` | boolean | no | Default: `false`. |
| `relations` | list<string> | no | Accepts multiple values as an array. |
| `uuid` | string | no |  |
| `externalId` | string | no |  |
| `name` | string | no |  |
| `description` | string | no |  |
| `state` | string | no |  |
| `usingSignature` | boolean | no |  |
| `usingSignatureMedia` | boolean | no |  |
| `usingBeehelp` | boolean | no |  |
| `subtractType` | string | no |  |
| `specialtyCode` | string | no |  |
| `certifType` | string | no |  |
| `certifLevel` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "certifLevel": "string",
      "certifType": "string",
      "conventions": [
        {}
      ],
      "convocations": [
        {}
      ],
      "creationDate": "2026-05-07T12:00:00.000Z",
      "deleteDate": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "endAt": "2026-05-07T12:00:00.000Z",
      "events": [
        {}
      ],
      "externalId": "string",
      "formation": {},
      "isAttestationDisabled": true,
      "isConventionDisabled": true,
      "isConvocationDisabled": true,
      "milestones": [
        {}
      ],
      "name": "Ava Chen",
      "pricing": {},
      "satisfaction": 1,
      "sessionDates": [
        {}
      ],
      "specialtyCode": "string",
      "startAt": "2026-05-07T12:00:00.000Z",
      "startedDate": "2026-05-07T12:00:00.000Z",
      "state": "string",
      "subtractType": "string",
      "updateDate": "2026-05-07T12:00:00.000Z",
      "usingBeehelp": true,
      "usingSignature": true,
      "usingSignatureMedia": true,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `certifLevel` | string | The certification level configured for the session |
| `certifType` | string | The certification type configured for the session |
| `conventions` | array<object> | The conventions linked to the session when requested |
| `convocations` | array<object> | The convocations linked to the session when requested |
| `creationDate` | date | The date when the session was created |
| `deleteDate` | date | The date when the session was deleted |
| `description` | string | The description of the session |
| `endAt` | date | The date of the last learning session date of this session |
| `events` | array<object> | The events linked to the session when requested |
| `externalId` | string | The id of the session in the external application (only for data importation) |
| `formation` | object | The formation linked to the session |
| `isAttestationDisabled` | boolean | Whether attestations are disabled for this session |
| `isConventionDisabled` | boolean | Whether conventions are disabled for this session |
| `isConvocationDisabled` | boolean | Whether convocations are disabled for this session |
| `milestones` | array<object> | The milestones linked to the session when requested |
| `name` | string | The name of the session |
| `pricing` | object | Pricing information for the session |
| `satisfaction` | number | The session satisfaction rate in percentage |
| `sessionDates` | array<object> | The learning session dates linked to the session when requested |
| `specialtyCode` | string | The specialty code configured for the session |
| `startAt` | date | The date of the first learning session date of this session |
| `startedDate` | date | The date when the session was started |
| `state` | string | The current state of the session |
| `subtractType` | string | The subtract type configured for the session |
| `updateDate` | date | The last date when the session was updated |
| `usingBeehelp` | boolean | Whether Beehelp is enabled for the session |
| `usingSignature` | boolean | Whether electronic signature for presences is enabled for the session |
| `usingSignatureMedia` | boolean | Whether electronic signature for documents is enabled for the session |
| `uuid` | string | The uuid of the session |

## Native endpoint

Through the native Qualiobee API, this operation is `GET /:organizationUuid/session` (base URL `https://app.qualiobee.fr/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sessions.md) for the provider-specific parameters and requirements.

