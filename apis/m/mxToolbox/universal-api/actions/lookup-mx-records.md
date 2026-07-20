# Mx Toolbox: Lookup MX Records



```
GET https://connect.mindcloud.co/v1/universal/mxToolbox/latest/actions/lookup-mx-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mx Toolbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mxToolbox/latest/actions/lookup-mx-records?connectionId=$CONNECTION_ID&domain=example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mxToolbox/latest/actions/lookup-mx-records?${params}`, {
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
| `domain` | string | yes | Domain to run the MX lookup against. Example: `example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "argumentType": "string",
      "command": "string",
      "commandArgument": "string",
      "errors": [
        {}
      ],
      "failed": [
        {}
      ],
      "hasSubscriptions": true,
      "information": [
        {}
      ],
      "isEndpoint": true,
      "isError": true,
      "passed": [
        {}
      ],
      "relatedLookups": [
        {}
      ],
      "reportingNameServer": "Ava Chen",
      "resourceRecordType": 1,
      "timeouts": [
        {}
      ],
      "timeRecorded": "2026-05-07T12:00:00.000Z",
      "timeToComplete": "string",
      "transcript": [
        {}
      ],
      "uid": "string",
      "warnings": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `argumentType` | string | Input type classified by MxToolbox. |
| `command` | string | Lookup command that handled the request. |
| `commandArgument` | string | Final lookup input sent to the provider. |
| `errors` | array<object> | Error entries returned by MxToolbox. |
| `failed` | array<object> | Failed checks returned by MxToolbox. |
| `hasSubscriptions` | boolean | Whether the target already has monitor subscriptions. |
| `information` | array<object> | Primary lookup result rows returned by MxToolbox. |
| `isEndpoint` | boolean | Whether the result refers to a direct endpoint target. |
| `isError` | boolean | Whether the lookup returned an error state. |
| `passed` | array<object> | Passing checks returned by MxToolbox. |
| `relatedLookups` | array<object> | Related MxToolbox lookups suggested by the provider. |
| `reportingNameServer` | string | Authoritative server reported by the lookup when available. |
| `resourceRecordType` | number | DNS record type identifier when available. |
| `timeouts` | array<object> | Timeout entries returned by MxToolbox. |
| `timeRecorded` | date | Provider timestamp for the lookup result. |
| `timeToComplete` | string | Provider-reported lookup duration in milliseconds. |
| `transcript` | array<object> | Diagnostic transcript from the provider. |
| `uid` | string | Provider request identifier when present. |
| `warnings` | array<object> | Warning checks returned by MxToolbox. |

## Native endpoint

Through the native Mx Toolbox API, this operation is `GET /lookup/mx` (base URL `https://api.mxtoolbox.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-mx-records.md) for the provider-specific parameters and requirements.

