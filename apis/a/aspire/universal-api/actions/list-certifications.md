# Aspire: List Certifications

Retrieves certifications from your Aspire account.

```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-certifications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-certifications?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-certifications?${params}`, {
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
| `expand` | string | no |  |
| `filter` | string | no |  |
| `orderBy` | string | no |  |
| `select` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CertificationDate": "2026-05-07T12:00:00.000Z",
      "CertificationID": 1,
      "CertificationTypeID": 1,
      "CertificationTypeName": "Ava Chen",
      "ContactID": 1,
      "ContactName": "Ava Chen",
      "CreatedByUserID": 1,
      "CreatedByUserName": "Ava Chen",
      "CreatedDateTime": "2026-05-07T12:00:00.000Z",
      "ExpirationDate": "2026-05-07T12:00:00.000Z",
      "LastModifiedByUserID": 1,
      "LastModifiedByUserName": "Ava Chen",
      "LastModifiedDateTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CertificationDate` | date |  |
| `CertificationID` | number |  |
| `CertificationTypeID` | number |  |
| `CertificationTypeName` | string |  |
| `ContactID` | number |  |
| `ContactName` | string |  |
| `CreatedByUserID` | number |  |
| `CreatedByUserName` | string |  |
| `CreatedDateTime` | date |  |
| `ExpirationDate` | date |  |
| `LastModifiedByUserID` | number |  |
| `LastModifiedByUserName` | string |  |
| `LastModifiedDateTime` | date |  |

## Native endpoint

Through the native Aspire API, this operation is `GET Certifications` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-certifications.md) for the provider-specific parameters and requirements.

