# ironSource: List Applications

Lists applications in ironSource.

```
GET https://connect.mindcloud.co/v1/universal/ironSource/latest/actions/list-applications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ironSource `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ironSource/latest/actions/list-applications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ironSource/latest/actions/list-applications?${params}`, {
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
| `appStatus` | string | no | Filter applications by activation status, such as active or archived. |
| `platform` | string | no | Filter applications by operating system: iOS or Android. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adUnits": {},
      "appKey": "string",
      "appName": "Ava Chen",
      "appStatus": "string",
      "bundleId": "string",
      "bundleRefId": 1,
      "ccpa": 1,
      "coppa": 1,
      "creationDate": "2026-05-07T12:00:00.000Z",
      "icon": "https://example.com",
      "networkReportingApi": {},
      "platform": "string",
      "taxonomy": "string",
      "trackId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adUnits` | object | Active ad network names by ad unit. |
| `appKey` | string | Application key as shown on the Unity LevelPlay platform. |
| `appName` | string | Application name. |
| `appStatus` | string | Application status, such as active or inactive. |
| `bundleId` | string | Store bundle ID. |
| `bundleRefId` | number | Bundle reference ID. |
| `ccpa` | number | CCPA setting where 1 is true and 0 is false. |
| `coppa` | number | COPPA setting where 1 is true and 0 is false. |
| `creationDate` | date | Date the application was added to the platform. |
| `icon` | string | Application icon URL from the store. |
| `networkReportingApi` | object | Reporting API verification status by network. |
| `platform` | string | Application platform, such as iOS or Android. |
| `taxonomy` | string | Application sub-genre. |
| `trackId` | string | Application store track ID for iOS apps. |

## Native endpoint

Through the native ironSource API, this operation is `GET partners/publisher/applications/v6` (base URL `https://platform.ironsrc.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-applications.md) for the provider-specific parameters and requirements.

