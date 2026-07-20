# Time Doctor: List Companies

Retrieves companies from Time Doctor.

```
GET https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/list-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Time Doctor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/list-companies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/list-companies?${params}`, {
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
      "allowManual": true,
      "company": {},
      "custom": {},
      "hiredAt": "2026-05-07T12:00:00.000Z",
      "isInteractive": true,
      "isSilent": true,
      "lastSeen": {},
      "name": "Ava Chen",
      "onlyProjectIds": [
        "string"
      ],
      "role": "string",
      "tagIds": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowManual` | boolean |  |
| `company` | object |  |
| `custom` | object |  |
| `hiredAt` | date |  |
| `isInteractive` | boolean |  |
| `isSilent` | boolean |  |
| `lastSeen` | object |  |
| `name` | string |  |
| `onlyProjectIds` | array<string> |  |
| `role` | string |  |
| `tagIds` | array<string> |  |

## Native endpoint

Through the native Time Doctor API, this operation is `GET /api/1.0/companies` (base URL `https://api2.timedoctor.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-companies.md) for the provider-specific parameters and requirements.

