# <img src="https://images.mindcloud.co/apps/icons/zoho-survey_1773680111282.png" alt="Zoho Survey logo" width="28" height="28"> Zoho Survey: Universal API

Send Zoho Survey email invitations using trigger-based distributions

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zohoSurvey/latest
- **Category:** Marketing
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://survey.zoho.com
- **Vendor API docs:** https://help.zoho.com/portal/en/kb/survey/launch/distribution

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get OAuth User Info](actions/get-oauth-user-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoSurvey/latest/actions/get-oauth-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get OAuth User Info](actions/get-oauth-user-info.md) | GET | Retrieves connected Zoho account user info for Zoho Survey. |

