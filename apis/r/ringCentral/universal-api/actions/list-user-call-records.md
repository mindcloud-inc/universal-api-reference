# RingCentral: List User Call Records

Returns call log records filtered by parameters specified.

```
GET https://connect.mindcloud.co/v1/universal/ringCentral/latest/actions/list-user-call-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RingCentral `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ringCentral/latest/actions/list-user-call-records?connectionId=$CONNECTION_ID&limit=25&offset=0&accountId=~&extensionId=~" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "accountId": "~",
  "extensionId": "~"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ringCentral/latest/actions/list-user-call-records?${params}`, {
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
| `accountId` | string | yes | Internal identifier of the RingCentral account. Default value is "~" to indicate that the account associated with current authorization session should be used. Example: `~`. |
| `extensionNumber` | string | no | Short extension number of a user. If specified, returns call log for this particular extension only. Cannot be combined with `phoneNumber` filter |
| `direction` | list<string> | no | The direction of call records to be included in the result. If omitted, both inbound and outbound calls are returned. |
| `type` | list<string> | no | The type of call records to be included in the result. If omitted, all call types are returned. |
| `view` | list<string> | no | Defines the level of details for returned call records. Example: `Simple`. |
| `withRecording` | boolean | no | Deprecated, replaced with `recordingType` filter, still supported for compatibility reasons. Indicates if only recorded calls should be returned. If both `withRecording` and `recordingType` parameters are specified, then `withRecording` is ignored |
| `recordingType` | list<string> | no | Indicates that call records with recordings of particular type should be returned. If omitted, then calls with and without recordings are returned. |
| `dateFrom` | string | no | The beginning of the time range to return call records in ISO 8601 format including timezone, for example `2016-03-10T18:07:52.534Z`. The default value is `dateTo` minus 24 hours |
| `dateTo` | string | no | The end of the time range to return call records in ISO 8601 format including timezone, for example `2016-03-10T18:07:52.534Z`. The default value is current time. |
| `sessionId` | string | no | Internal identifier of a call session. |
| `telephonySessionId` | string | no | Internal identifier of a telephony session. |
| `metadataCategory` | string | no | Accepts multiple values as an array. |
| `showDeleted` | boolean | no | Indicates that deleted calls records should be returned |
| `extensionId` | string | yes | Internal identifier of the RingCentral extension. Default value is "~" to indicate that the extension associated with current authorization session should be used. Example: `~`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": "string",
      "billing": {
        "costIncluded": 1,
        "costPurchased": 1
      },
      "direction": "string",
      "duration": 1,
      "durationMs": 1,
      "from": {
        "location": "string",
        "name": "Ava Chen",
        "phoneNumber": "string"
      },
      "id": "string",
      "internalType": "string",
      "lastModifiedTime": "string",
      "legs": [
        {
          "action": "string",
          "billing": {
            "costIncluded": 1,
            "costPurchased": 1
          },
          "direction": "string",
          "duration": 1,
          "durationMs": 1,
          "from": {
            "location": "string",
            "name": "Ava Chen",
            "phoneNumber": "string"
          },
          "internalType": "string",
          "legType": "string",
          "master": true,
          "partyId": "string",
          "result": "string",
          "startTime": "string",
          "telephonySessionId": "string",
          "to": {
            "phoneNumber": "string"
          },
          "transport": "string",
          "type": "string"
        }
      ],
      "partyId": "string",
      "result": "string",
      "sessionId": "string",
      "startTime": "string",
      "telephonySessionId": "string",
      "to": {
        "phoneNumber": "string"
      },
      "transport": "string",
      "type": "string",
      "uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | string |  |
| `billing.costIncluded` | number |  |
| `billing.costPurchased` | number |  |
| `direction` | string |  |
| `duration` | number |  |
| `durationMs` | number |  |
| `from.location` | string |  |
| `from.name` | string |  |
| `from.phoneNumber` | string |  |
| `id` | string |  |
| `internalType` | string |  |
| `lastModifiedTime` | string |  |
| `legs[].action` | string |  |
| `legs[].billing.costIncluded` | number |  |
| `legs[].billing.costPurchased` | number |  |
| `legs[].direction` | string |  |
| `legs[].duration` | number |  |
| `legs[].durationMs` | number |  |
| `legs[].from.location` | string |  |
| `legs[].from.name` | string |  |
| `legs[].from.phoneNumber` | string |  |
| `legs[].internalType` | string |  |
| `legs[].legType` | string |  |
| `legs[].master` | boolean |  |
| `legs[].partyId` | string |  |
| `legs[].result` | string |  |
| `legs[].startTime` | string |  |
| `legs[].telephonySessionId` | string |  |
| `legs[].to.phoneNumber` | string |  |
| `legs[].transport` | string |  |
| `legs[].type` | string |  |
| `partyId` | string |  |
| `result` | string |  |
| `sessionId` | string |  |
| `startTime` | string |  |
| `telephonySessionId` | string |  |
| `to.phoneNumber` | string |  |
| `transport` | string |  |
| `type` | string |  |
| `uri` | string |  |

## Native endpoint

Through the native RingCentral API, this operation is `GET restapi/v1.0/account/:accountId/extension/:extensionId/call-log` (base URL `https://platform.ringcentral.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-user-call-records.md) for the provider-specific parameters and requirements.

