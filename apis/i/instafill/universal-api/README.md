# <img src="https://images.mindcloud.co/apps/icons/instafill_1775823352551.png" alt="Instafill logo" width="28" height="28"> Instafill: Universal API

Upload forms, manage reusable profiles, create filling sessions, and run PDF utility workflows with Instafill.ai.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/instafill/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 28
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://instafill.ai
- **Vendor API docs:** https://docs.instafill.ai/docs/api/intro

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Details](actions/get-account-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instafill/latest/actions/get-account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (28)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Details](actions/get-account-details.md) | GET |  |

### Conversion Job

| Action | Method | Description |
| --- | --- | --- |
| [Convert Form](actions/convert-form.md) | POST |  |
| [Get Conversion Status](actions/get-conversion-status.md) | GET |  |

### Flat Check

| Action | Method | Description |
| --- | --- | --- |
| [Check Flat PDF](actions/check-flat.md) | POST |  |

### Form

| Action | Method | Description |
| --- | --- | --- |
| [Get Form](actions/get-form.md) | GET |  |
| [List Forms](actions/list-forms.md) | GET |  |
| [Search Forms](actions/search-forms.md) | GET |  |
| [Upload Form](actions/upload-form.md) | POST |  |

### Make Hook

| Action | Method | Description |
| --- | --- | --- |
| [Delete Make Hook](actions/delete-make-hook.md) | DELETE |  |
| [Subscribe Make Hook](actions/subscribe-make-hook.md) | POST |  |

### N8n Hook

| Action | Method | Description |
| --- | --- | --- |
| [Delete n8n Hook](actions/delete-n8n-hook.md) | DELETE |  |
| [Subscribe n8n Hook](actions/subscribe-n8n-hook.md) | POST |  |

### Power Automate Hook

| Action | Method | Description |
| --- | --- | --- |
| [Delete Power Automate Hook](actions/delete-power-automate-hook.md) | DELETE |  |
| [Subscribe Power Automate Hook](actions/subscribe-power-automate-hook.md) | POST |  |

### Profile

| Action | Method | Description |
| --- | --- | --- |
| [Create Profile](actions/create-profile.md) | POST |  |
| [Delete Profile](actions/delete-profile.md) | DELETE |  |
| [Get Profile](actions/get-profile.md) | GET |  |
| [List Profiles](actions/list-profiles.md) | GET |  |
| [Update Profile Name](actions/update-profile-name.md) | PUT |  |
| [Update Profile Text Info](actions/update-profile-text-info.md) | PUT |  |

### Profile File

| Action | Method | Description |
| --- | --- | --- |
| [Delete Profile File](actions/delete-profile-file.md) | DELETE |  |
| [Upload Profile File](actions/upload-profile-file.md) | POST |  |

### Session

| Action | Method | Description |
| --- | --- | --- |
| [Create Session](actions/create-session.md) | POST |  |
| [Get Session](actions/get-session.md) | GET |  |
| [List Sessions](actions/list-sessions.md) | GET |  |

### Zapier Hook

| Action | Method | Description |
| --- | --- | --- |
| [Delete Zapier Hook](actions/delete-zapier-hook.md) | DELETE |  |
| [Subscribe Zapier Hook](actions/subscribe-zapier-hook.md) | POST |  |

### Zapier Hook Sample

| Action | Method | Description |
| --- | --- | --- |
| [Get Zapier Hook Sample](actions/get-zapier-hook-sample.md) | GET |  |

