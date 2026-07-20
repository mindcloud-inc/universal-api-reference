# Amazing Marvin: Get Account Information

Retrieves account information from Amazing Marvin.

```
GET https://connect.mindcloud.co/v1/universal/amazingMarvin/latest/actions/get-account-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazing Marvin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amazingMarvin/latest/actions/get-account-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amazingMarvin/latest/actions/get-account-information?${params}`, {
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
      "billingPeriod": "string",
      "currentVersion": "string",
      "defaultAutoSnooze": true,
      "defaultOffset": 1,
      "defaultSnooze": 1,
      "email": "ava@example.com",
      "emailConfirmed": true,
      "iosSub": true,
      "marvinPoints": 1,
      "nextMultiplier": 1,
      "paidThrough": "2026-05-07T12:00:00.000Z",
      "parentEmail": "ava@example.com",
      "rewardPointsEarned": 1,
      "rewardPointsEarnedToday": 1,
      "rewardPointsLastDate": "2026-05-07T12:00:00.000Z",
      "rewardPointsSpent": 1,
      "rewardPointsSpentToday": 1,
      "signupAppVersion": "string",
      "tomatoDate": "string",
      "tomatoes": 1,
      "tomatoesToday": 1,
      "tomatoTime": 1,
      "tomatoTimeToday": 1,
      "tracking": "string",
      "trackingSince": 1,
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingPeriod` | string |  |
| `currentVersion` | string |  |
| `defaultAutoSnooze` | boolean |  |
| `defaultOffset` | number |  |
| `defaultSnooze` | number |  |
| `email` | string |  |
| `emailConfirmed` | boolean |  |
| `iosSub` | boolean |  |
| `marvinPoints` | number |  |
| `nextMultiplier` | number |  |
| `paidThrough` | date |  |
| `parentEmail` | string |  |
| `rewardPointsEarned` | number |  |
| `rewardPointsEarnedToday` | number |  |
| `rewardPointsLastDate` | date |  |
| `rewardPointsSpent` | number |  |
| `rewardPointsSpentToday` | number |  |
| `signupAppVersion` | string |  |
| `tomatoDate` | string |  |
| `tomatoes` | number |  |
| `tomatoesToday` | number |  |
| `tomatoTime` | number |  |
| `tomatoTimeToday` | number |  |
| `tracking` | string |  |
| `trackingSince` | number |  |
| `userId` | string |  |

## Native endpoint

Through the native Amazing Marvin API, this operation is `GET /me` (base URL `https://serv.amazingmarvin.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-information.md) for the provider-specific parameters and requirements.

