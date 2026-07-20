# MOBIDI: Get Next Or Previous Record

Retrieves the next or previous record in MOBIDI.

```
GET https://connect.mindcloud.co/v1/universal/mOBIDI/latest/actions/get-next-or-previous-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MOBIDI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mOBIDI/latest/actions/get-next-or-previous-record?connectionId=$CONNECTION_ID&currentRecordId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "currentRecordId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mOBIDI/latest/actions/get-next-or-previous-record?${params}`, {
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
| `currentRecordId` | string | yes | Current MOBIDI record identifier. |
| `isMap` | boolean | no | Whether to use map navigation mode. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Next": "string",
      "Prev": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Next` | string | Next record identifier. |
| `Prev` | string | Previous record identifier. |

## Native endpoint

Through the native MOBIDI API, this operation is `POST /MobidiQueryManagerHandler` (base URL `https://servis2.dece.com.tr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-next-or-previous-record.md) for the provider-specific parameters and requirements.

