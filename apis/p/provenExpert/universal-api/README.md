# <img src="https://images.mindcloud.co/apps/icons/proven-expert_1774891930036.png" alt="ProvenExpert logo" width="28" height="28"> ProvenExpert: Universal API

Collect reviews, send invites, and share rating widgets

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/provenExpert/latest
- **Category:** Marketing
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.provenexpert.com
- **Vendor API docs:** https://developer.provenexpert.com/index_en.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Profile](actions/get-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/get-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Api Credentials

| Action | Method | Description |
| --- | --- | --- |
| [Get API Credentials](actions/get-api-credentials.md) | GET | Retrieves your ProvenExpert API credentials. |
| [List Child API Credentials](actions/list-child-api-credentials.md) | GET | Lists API credentials for child profiles in ProvenExpert. |

### Invitation Link

| Action | Method | Description |
| --- | --- | --- |
| [Create Invitation Link](actions/create-invitation-link.md) | POST | Creates a personal survey invitation link in ProvenExpert. |
| [List Invitation Links](actions/list-invitation-links.md) | GET | Lists survey invitation links in ProvenExpert. |

### Invitation Mailing

| Action | Method | Description |
| --- | --- | --- |
| [Create Invitation Mail](actions/create-invitation-mail.md) | POST | Creates and sends survey invitation emails in ProvenExpert. |
| [Get Invitation Mail Status](actions/get-invitation-mail-status.md) | GET | Retrieves the status of an invitation mailing in ProvenExpert. |

### Login Url

| Action | Method | Description |
| --- | --- | --- |
| [Get Login URL](actions/get-login-url.md) | GET | Retrieves a single sign-on login URL from ProvenExpert. |

### Profile

| Action | Method | Description |
| --- | --- | --- |
| [Create Profile](actions/create-profile.md) | POST | Creates a profile in ProvenExpert. |
| [Get Profile](actions/get-profile.md) | GET | Retrieves your profile from ProvenExpert. |
| [List Child Profiles](actions/list-child-profiles.md) | GET | Lists child profiles in ProvenExpert. |
| [Update Profile](actions/update-profile.md) | PUT | Updates your profile in ProvenExpert. |

### Profile Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get Profile Settings](actions/get-profile-settings.md) | GET | Retrieves your profile settings from ProvenExpert. |
| [Update Profile Settings](actions/update-profile-settings.md) | PUT | Updates your profile settings in ProvenExpert. |

### Rating Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Rating Summary](actions/get-rating-summary.md) | GET | Retrieves your profile rating summary from ProvenExpert. |
| [Get Rich Snippet](actions/get-rich-snippet.md) | GET | Retrieves rich snippet HTML for ProvenExpert ratings. |
| [List Child Rating Summaries](actions/list-child-rating-summaries.md) | GET | Lists child profile rating summaries in ProvenExpert. |

### Survey

| Action | Method | Description |
| --- | --- | --- |
| [Create Survey](actions/create-survey.md) | POST | Creates a survey in ProvenExpert. |
| [List Surveys](actions/list-surveys.md) | GET | Lists your surveys in ProvenExpert. |
| [Update Survey](actions/update-survey.md) | PUT | Updates an existing survey in ProvenExpert. |

### Widget

| Action | Method | Description |
| --- | --- | --- |
| [Create Widget](actions/create-widget.md) | POST | Creates a widget in ProvenExpert. |

