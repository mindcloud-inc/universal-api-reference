# BippyBox: Get User Data

Retrieves BippyBox account data, devices, colors, and audio files.

```
GET https://connect.mindcloud.co/v1/universal/bippyBox/latest/actions/get-user-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BippyBox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bippyBox/latest/actions/get-user-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bippyBox/latest/actions/get-user-data?${params}`, {
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
      "audioFiles": [
        {}
      ],
      "claimedDevices": [
        {}
      ],
      "colors": [
        {}
      ],
      "createdAt": {
        "_nanoseconds": 1,
        "_seconds": 1
      },
      "email": "ava@example.com",
      "firstname": "Ava",
      "isAdmin": true,
      "lastname": "Chen",
      "thingsboardCustomerId": "string",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audioFiles` | array<object> | Uploaded audio files available to the account. |
| `claimedDevices` | array<object> | Connected BippyBox devices claimed by the account. |
| `colors` | array<object> | Saved trigger colors for the account. |
| `createdAt` | object | Firestore-style account creation timestamp object. |
| `createdAt._nanoseconds` | number | Creation timestamp nanoseconds component. |
| `createdAt._seconds` | number | Creation timestamp seconds component. |
| `email` | string | The email address on the BippyBox account. |
| `firstname` | string | The account first name. |
| `isAdmin` | boolean | Whether the user has admin privileges. |
| `lastname` | string | The account last name. |
| `thingsboardCustomerId` | string | The linked ThingsBoard customer identifier. |
| `uid` | string | The BippyBox user UID. |

## Native endpoint

Through the native BippyBox API, this operation is `GET /getuserdata` (base URL `https://app.bippybox.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-data.md) for the provider-specific parameters and requirements.

