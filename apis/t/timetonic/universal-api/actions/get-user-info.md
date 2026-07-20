# Timetonic: Get User Info

Retrieves the current user information from Timetonic.

```
GET https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/get-user-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timetonic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/get-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/get-user-info?${params}`, {
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
| `syncStamp` | string | no | Optional sync stamp for incremental reads. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdVNB": "string",
      "req": "string",
      "sstamp": 1,
      "status": "string",
      "transactionId": "string",
      "userInfo": {
        "colors": {
          "bleuNuit": "string",
          "bleuTurquoise": "string",
          "bleuViolet": "string",
          "defaut": "string",
          "gray": "string",
          "green": "string",
          "jauneIndien": "string",
          "lilas": "string",
          "noir": "string",
          "orange": "string",
          "orangePastel": "string",
          "pink": "string",
          "red": "string",
          "roseBois": "string",
          "vertPastel": "string"
        },
        "companyAccountPlan": "string",
        "firstTime": true,
        "licence": "string",
        "nbBooks": 1,
        "projectID": 1,
        "rights": {
          "canCreateWorkspace": true
        },
        "sstamp": 1,
        "uC": "string",
        "uimgStamp": 1,
        "userPrefs": {
          "account": "string",
          "address": "string",
          "birthd": "string",
          "cie": "string",
          "city": "string",
          "companySize": "string",
          "country": "string",
          "fname": "Ava Chen",
          "globalAdd": true,
          "globalCalendar": true,
          "globalSearch": true,
          "ip": "string",
          "lang": "string",
          "lastConnection": "string",
          "licenceId": 1,
          "lname": "Ava Chen",
          "mail1": "string",
          "mail1ToConfirm": "string",
          "mail2": "string",
          "mail2ToConfirm": "string",
          "method": "string",
          "mob1": "string",
          "mob2": "string",
          "nbCol": 1,
          "newsletter": true,
          "notifMobile": "string",
          "openGrand": true,
          "origin": "string",
          "region": "string",
          "regiondf": "string",
          "replace": true,
          "sdate": "string",
          "secondsSincePreviousConnection": "string",
          "sector": {},
          "sex": "string",
          "slashd": true,
          "soundNotifications": true,
          "syncWithHubic": true,
          "timezone": "string",
          "twoFactor": true,
          "twoFactorSecret": "string",
          "tz": "string",
          "ucreatedon": "string",
          "ukey": "string",
          "until": "string",
          "vatn": "string",
          "zip": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdVNB` | string |  |
| `req` | string |  |
| `sstamp` | number |  |
| `status` | string |  |
| `transactionId` | string |  |
| `userInfo.colors.bleuNuit` | string |  |
| `userInfo.colors.bleuTurquoise` | string |  |
| `userInfo.colors.bleuViolet` | string |  |
| `userInfo.colors.defaut` | string |  |
| `userInfo.colors.gray` | string |  |
| `userInfo.colors.green` | string |  |
| `userInfo.colors.jauneIndien` | string |  |
| `userInfo.colors.lilas` | string |  |
| `userInfo.colors.noir` | string |  |
| `userInfo.colors.orange` | string |  |
| `userInfo.colors.orangePastel` | string |  |
| `userInfo.colors.pink` | string |  |
| `userInfo.colors.red` | string |  |
| `userInfo.colors.roseBois` | string |  |
| `userInfo.colors.vertPastel` | string |  |
| `userInfo.companyAccountPlan` | string |  |
| `userInfo.firstTime` | boolean |  |
| `userInfo.licence` | string |  |
| `userInfo.nbBooks` | number |  |
| `userInfo.projectID` | number |  |
| `userInfo.rights.canCreateWorkspace` | boolean |  |
| `userInfo.sstamp` | number |  |
| `userInfo.uC` | string |  |
| `userInfo.uimgStamp` | number |  |
| `userInfo.userPrefs.account` | string |  |
| `userInfo.userPrefs.address` | string |  |
| `userInfo.userPrefs.birthd` | string |  |
| `userInfo.userPrefs.cie` | string |  |
| `userInfo.userPrefs.city` | string |  |
| `userInfo.userPrefs.companySize` | string |  |
| `userInfo.userPrefs.country` | string |  |
| `userInfo.userPrefs.fname` | string |  |
| `userInfo.userPrefs.globalAdd` | boolean |  |
| `userInfo.userPrefs.globalCalendar` | boolean |  |
| `userInfo.userPrefs.globalSearch` | boolean |  |
| `userInfo.userPrefs.ip` | string |  |
| `userInfo.userPrefs.lang` | string |  |
| `userInfo.userPrefs.lastConnection` | string |  |
| `userInfo.userPrefs.licenceId` | number |  |
| `userInfo.userPrefs.lname` | string |  |
| `userInfo.userPrefs.mail1` | string |  |
| `userInfo.userPrefs.mail1ToConfirm` | string |  |
| `userInfo.userPrefs.mail2` | string |  |
| `userInfo.userPrefs.mail2ToConfirm` | string |  |
| `userInfo.userPrefs.method` | string |  |
| `userInfo.userPrefs.mob1` | string |  |
| `userInfo.userPrefs.mob2` | string |  |
| `userInfo.userPrefs.nbCol` | number |  |
| `userInfo.userPrefs.newsletter` | boolean |  |
| `userInfo.userPrefs.notifMobile` | string |  |
| `userInfo.userPrefs.openGrand` | boolean |  |
| `userInfo.userPrefs.origin` | string |  |
| `userInfo.userPrefs.region` | string |  |
| `userInfo.userPrefs.regiondf` | string |  |
| `userInfo.userPrefs.replace` | boolean |  |
| `userInfo.userPrefs.sdate` | string |  |
| `userInfo.userPrefs.secondsSincePreviousConnection` | string |  |
| `userInfo.userPrefs.sector` | object |  |
| `userInfo.userPrefs.sex` | string |  |
| `userInfo.userPrefs.slashd` | boolean |  |
| `userInfo.userPrefs.soundNotifications` | boolean |  |
| `userInfo.userPrefs.syncWithHubic` | boolean |  |
| `userInfo.userPrefs.timezone` | string |  |
| `userInfo.userPrefs.twoFactor` | boolean |  |
| `userInfo.userPrefs.twoFactorSecret` | string |  |
| `userInfo.userPrefs.tz` | string |  |
| `userInfo.userPrefs.ucreatedon` | string |  |
| `userInfo.userPrefs.ukey` | string |  |
| `userInfo.userPrefs.until` | string |  |
| `userInfo.userPrefs.vatn` | string |  |
| `userInfo.userPrefs.zip` | string |  |

## Native endpoint

Through the native Timetonic API, this operation is `POST` (base URL `https://timetonic.com/live/api.php`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-info.md) for the provider-specific parameters and requirements.

