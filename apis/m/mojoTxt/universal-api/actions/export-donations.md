# MojoTxt: Export Donations

Retrieves a donation export from MojoTxt.

```
GET https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/export-donations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MojoTxt `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/export-donations?connectionId=$CONNECTION_ID&limit=25&offset=0&donationIdOrKeyword=string&phoneNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "donationIdOrKeyword": "string",
  "phoneNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/export-donations?${params}`, {
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
| `donationIdOrKeyword` | string | yes | The donation keyword identifier or keyword value to export. |
| `endTime` | string | no | Return donation transactions on or before this UNIX timestamp. |
| `getPerson` | string | no | Set to 1 to include donor contact information in the export. |
| `phoneNumber` | string | yes | The MojoTxt phone number in international format, like +17792533748. |
| `startTime` | string | no | Return donation transactions on or after this UNIX timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "record_count": 1,
      "result": "string",
      "timestamp": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `record_count` | number | The number of export rows returned. |
| `result` | string | Whether the export request succeeded. |
| `timestamp` | number | MojoTxt server timestamp for the response. |

## Native endpoint

Through the native MojoTxt API, this operation is `GET /:phoneNumber/donations/export/:donationIdOrKeyword` (base URL `https://app.mojotxt.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/export-donations.md) for the provider-specific parameters and requirements.

