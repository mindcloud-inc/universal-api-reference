# CoachAccountable: List Agreements

Retrieves agreements from CoachAccountable.

```
GET https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-agreements
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoachAccountable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-agreements?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-agreements?${params}`, {
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
| `clientId` | number | no | Filter to Agreements belonging to a specific client. |
| `title` | string | no | Filter Agreements by which title, prefixed. |
| `includeContent` | boolean | no | Set to true to include the full HTML content of the Agreements. Default: `false`. |
| `which` | list | no | Filter by Agreement status. One of: `A`, `B`, `O`. Default: `A`. |
| `dateFrom` | date | no | Set to restrict Agreements returned to those issued at or after the provided value. |
| `dateTo` | date | no | Set to restrict Agreements returned to those issued at or before the provided value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ClientID": 1,
      "content": "string",
      "dateAgreed": "2026-05-07T12:00:00.000Z",
      "dateIssued": "2026-05-07T12:00:00.000Z",
      "ID": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ClientID` | number |  |
| `content` | string |  |
| `dateAgreed` | date |  |
| `dateIssued` | date |  |
| `ID` | number |  |
| `title` | string |  |

## Native endpoint

Through the native CoachAccountable API, this operation is `POST /` (base URL `https://www.coachaccountable.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-agreements.md) for the provider-specific parameters and requirements.

