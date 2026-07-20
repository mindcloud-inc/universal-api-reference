# TaxBandits: List Record IDs by Submission ID

Retrieves record IDs for a submission in TaxBandits.

```
GET https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/list-record-ids-by-submission-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TaxBandits `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/list-record-ids-by-submission-id?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/list-record-ids-by-submission-id?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "Errors": [
        {}
      ],
      "RecordIds": [
        "string"
      ],
      "StatusCode": 1,
      "StatusMessage": "string",
      "StatusName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Errors` | array<object> |  |
| `RecordIds` | array<string> |  |
| `StatusCode` | number |  |
| `StatusMessage` | string |  |
| `StatusName` | string |  |

## Native endpoint

Through the native TaxBandits API, this operation is `GET Utility/GetRecordIdBySubmissionId` (base URL `https://testapi.taxbandits.com/v1.7.3/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-record-ids-by-submission-id.md) for the provider-specific parameters and requirements.

