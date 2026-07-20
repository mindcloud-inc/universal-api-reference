# ProvenExpert: Update Profile Settings

Updates your profile settings in ProvenExpert.

```
PUT https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/update-profile-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProvenExpert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/update-profile-settings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/update-profile-settings', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data.public` | number | no | Whether the profile should be public after the settings update. Example: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "mails": {
        "newsletter": 1,
        "reporting": 1
      },
      "notify": {
        "contactRequest": 1,
        "externalRating": 1,
        "inviteConfirmation": 1,
        "rating": 1,
        "ratingRequest": 1,
        "service": 1
      },
      "privacy": {
        "contactButton": 1,
        "ratingButton": 1,
        "ratingButtonWithCode": 1,
        "showAllCompetences": 1,
        "showCompanyName": 1,
        "showExternalRatings": 1,
        "showLastname": 1,
        "showName": 1,
        "showRatingCompetences": 1,
        "showTopCompetences": 1,
        "showVoterData": 1
      },
      "public": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `mails.newsletter` | number | Whether newsletter emails are enabled. |
| `mails.reporting` | number | Whether reporting emails are enabled. |
| `notify.contactRequest` | number | Whether contact request notifications are enabled. |
| `notify.externalRating` | number | Whether external rating notifications are enabled. |
| `notify.inviteConfirmation` | number | Whether invite confirmation notifications are enabled. |
| `notify.rating` | number | Whether rating notifications are enabled. |
| `notify.ratingRequest` | number | Whether rating request notifications are enabled. |
| `notify.service` | number | Whether service notifications are enabled. |
| `privacy.contactButton` | number | Whether the public contact button is enabled. |
| `privacy.ratingButton` | number | Whether the public rating button is enabled. |
| `privacy.ratingButtonWithCode` | number | Whether the rating button with code is enabled. |
| `privacy.showAllCompetences` | number | Whether all competences are shown. |
| `privacy.showCompanyName` | number | Whether the company name is shown publicly. |
| `privacy.showExternalRatings` | number | Whether external ratings are shown. |
| `privacy.showLastname` | number | Whether reviewer last names are shown publicly. |
| `privacy.showName` | number | Whether reviewer first names are shown publicly. |
| `privacy.showRatingCompetences` | number | Whether rating competences are shown. |
| `privacy.showTopCompetences` | number | Whether top competences are shown. |
| `privacy.showVoterData` | number | Whether voter data is shown publicly. |
| `public` | number | Profile visibility flag returned by ProvenExpert settings. |

## Native endpoint

Through the native ProvenExpert API, this operation is `POST /profile/settings/update` (base URL `https://www.provenexpert.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-profile-settings.md) for the provider-specific parameters and requirements.

