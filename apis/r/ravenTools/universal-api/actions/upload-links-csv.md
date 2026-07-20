# Raven Tools: Upload Links CSV

Uploads links from a CSV file to Raven Tools.

```
POST https://connect.mindcloud.co/v1/universal/ravenTools/latest/actions/upload-links-csv
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raven Tools `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ravenTools/latest/actions/upload-links-csv" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "domain": "mindcloud.co",
  "file": "c3RhdHVzLGxpbmsgdHlwZSxsaW5rIHRleHQsbGluayB1cmwsd2Vic2l0ZSB1cmwsd2Vic2l0ZSB0eXBlLHRhZ3MKYWN0aXZlLE9yZ2FuaWMsVXBsb2FkZWQgUmF2ZW4gTGluayxodHRwczovL21pbmRjbG91ZC5jbyxodHRwczovL2V4YW1wbGUuY29tL3VwbG9hZGVkLE90aGVyLCJ1cGxvYWQsdGVzdCINCg=="
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ravenTools/latest/actions/upload-links-csv', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "domain": "mindcloud.co",
    "file": "c3RhdHVzLGxpbmsgdHlwZSxsaW5rIHRleHQsbGluayB1cmwsd2Vic2l0ZSB1cmwsd2Vic2l0ZSB0eXBlLHRhZ3MKYWN0aXZlLE9yZ2FuaWMsVXBsb2FkZWQgUmF2ZW4gTGluayxodHRwczovL21pbmRjbG91ZC5jbyxodHRwczovL2V4YW1wbGUuY29tL3VwbG9hZGVkLE90aGVyLCJ1cGxvYWQsdGVzdCINCg=="
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domain` | string | yes | The domain whose links should receive the CSV import. Default: `codex-raven-tools-verify-20260408.example`. Example: `mindcloud.co`. |
| `monitor` | string | no | Set to 1 to enable link monitoring for uploaded links. Example: `1`. |
| `file` | file | yes | Base64-encoded CSV content to upload to Raven Tools. Default: `c3RhdHVzLGxpbmsgdHlwZSxsaW5rIHRleHQsbGluayB1cmwsd2Vic2l0ZSB1cmwsd2Vic2l0ZSB0eXBlLHRhZ3MKYWN0aXZlLE9yZ2FuaWMsVXBsb2FkZWQgUmF2ZW4gTGluayxodHRwczovL21pbmRjbG91ZC5jbyxodHRwczovL2V4YW1wbGUuY29tL3VwbG9hZGVkLE90aGVyLCJ1cGxvYWQsdGVzdCINCg==`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | Imported Raven link id. |

## Native endpoint

Through the native Raven Tools API, this operation is `POST /api` (base URL `https://api.raventools.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-links-csv.md) for the provider-specific parameters and requirements.

