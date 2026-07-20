# Routee: Retrieve all the Pools of an account

Retrieves all the pools of an account from Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-all-the-pools-of-an-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-all-the-pools-of-an-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-all-the-pools-of-an-account?${params}`, {
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
      "content": [
        [
          {}
        ]
      ],
      "first": true,
      "last": true,
      "number": 1,
      "numberOfElements": 1,
      "size": 1,
      "totalElements": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content[]` | array<object> |  |
| `content[].poolId` | string |  |
| `content[].poolName` | string |  |
| `content[].smsSettings` | object |  |
| `content[].smsSettings.defaultCountry` | string |  |
| `content[].smsSettings.geomatch` | boolean |  |
| `content[].smsSettings.multipleSender[]` | array<object> |  |
| `content[].smsSettings.multipleSender[].country` | string |  |
| `content[].smsSettings.multipleSender[].keyword` | string |  |
| `content[].smsSettings.multipleSender[].senderId` | string |  |
| `content[].smsSettings.sticky` | boolean |  |
| `content[].smsSettings.transcode` | boolean |  |
| `content[].totalNumbers` | number |  |
| `content[].updatedAt` | string |  |
| `first` | boolean |  |
| `last` | boolean |  |
| `number` | number |  |
| `numberOfElements` | number |  |
| `size` | number |  |
| `totalElements` | number |  |
| `totalPages` | number |  |

## Native endpoint

Through the native Routee API, this operation is `GET /pools/my` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-all-the-pools-of-an-account.md) for the provider-specific parameters and requirements.

