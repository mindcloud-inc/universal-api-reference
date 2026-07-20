# Envoice: Get Work Type Details

Retrieves work type details from Envoice.

```
GET https://connect.mindcloud.co/v1/universal/envoice/latest/actions/get-work-type-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Envoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/envoice/latest/actions/get-work-type-details?connectionId=$CONNECTION_ID&workTypeId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workTypeId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/envoice/latest/actions/get-work-type-details?${params}`, {
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
| `workTypeId` | number | yes | Work type identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CreatedOn": "2026-05-07T12:00:00.000Z",
      "ErrorMessages": [
        "string"
      ],
      "Id": 1,
      "IsFaulted": true,
      "Title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CreatedOn` | date | Work type creation timestamp. |
| `ErrorMessages` | array<string> | Error messages returned by Envoice. |
| `Id` | number | Work type identifier. |
| `IsFaulted` | boolean | Whether the request failed. |
| `Title` | string | Work type title. |

## Native endpoint

Through the native Envoice API, this operation is `GET worktype/details` (base URL `https://www.envoice.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-work-type-details.md) for the provider-specific parameters and requirements.

