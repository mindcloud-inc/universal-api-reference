# <img src="https://images.mindcloud.co/apps/icons/florm-icon_1775490996510.png" alt="Florm logo" width="28" height="28"> Florm: Universal API

Build, manage, analyze, and export Florm forms, responses, and workspace analytics.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/florm/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 27
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://florm.io
- **Vendor API docs:** https://api.florm.io/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get My Profile](actions/get-my-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/florm/latest/actions/get-my-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (27)

### Access Token

| Action | Method | Description |
| --- | --- | --- |
| [Get Demo Token](actions/get-demo-token.md) | GET | Retrieves a demo access token from Florm. |
| [Refresh Access Token](actions/refresh-access-token.md) | GET | Refreshes an access token in Florm. |

### Design Theme

| Action | Method | Description |
| --- | --- | --- |
| [List Public Design Themes](actions/list-public-design-themes.md) | GET | Retrieves public design themes from Florm. |

### Export Task

| Action | Method | Description |
| --- | --- | --- |
| [Export Form Analytics](actions/export-form-analytics.md) | POST | Creates an export task for Florm form analytics. |
| [Export Form Answers](actions/export-form-answers.md) | POST | Creates an export task for Florm form answers. |
| [Export Form Step Answers](actions/export-form-step-answers.md) | POST | Creates an export task for Florm form step answers. |
| [Get Export Task](actions/get-export-task.md) | GET | Retrieves a specific Florm export task. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Get Form QR Code](actions/get-form-qr-code.md) | GET | Retrieves a QR code for a Florm form. |

### Form

| Action | Method | Description |
| --- | --- | --- |
| [Copy Form](actions/copy-form.md) | POST | Creates a copy of a Florm form. |
| [Create Form](actions/create-form.md) | POST | Creates a new form in Florm. |
| [Delete Form](actions/delete-form.md) | DELETE | Deletes an existing form from Florm. |
| [Get Form](actions/get-form.md) | GET | Retrieves a specific form from Florm. |
| [List Forms](actions/list-forms.md) | GET | Retrieves forms from your Florm workspace. |
| [Update Form](actions/update-form.md) | PUT | Updates an existing form in Florm. |

### Form Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Form Analytics](actions/get-form-analytics.md) | GET | Retrieves analytics for a Florm form. |

### Form Analytics Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Form Analytics Summary](actions/get-form-analytics-summary.md) | GET | Retrieves analytics summary for a Florm form. |

### Form Answer List

| Action | Method | Description |
| --- | --- | --- |
| [List Form Answers](actions/list-form-answers.md) | GET | Retrieves answers for a Florm form. |

### Form Step Answer List

| Action | Method | Description |
| --- | --- | --- |
| [List Form Step Answers](actions/list-form-step-answers.md) | GET | Retrieves answers for a Florm form step. |

### Magic Link

| Action | Method | Description |
| --- | --- | --- |
| [Create Magic Link](actions/create-magic-link.md) | POST | Creates a login magic link in Florm. |

### Session

| Action | Method | Description |
| --- | --- | --- |
| [Login With Magic Link](actions/login-with-magic-link.md) | GET | Logs into Florm with a magic link. |
| [Logout](actions/logout.md) | DELETE | Logs out the current Florm session. |

### Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Healthcheck](actions/get-healthcheck.md) | GET | Retrieves the current Florm healthcheck status. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Get My Team](actions/get-my-team.md) | GET | Retrieves your current team from Florm. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get My Profile](actions/get-my-profile.md) | GET | Retrieves your user profile from Florm. |
| [Update My Profile](actions/update-my-profile.md) | PUT | Updates your user profile in Florm. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Get My Workspace](actions/get-my-workspace.md) | GET | Retrieves your private workspace from Florm. |

### Workspace Metric

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspace Metrics](actions/get-workspace-metrics.md) | GET | Retrieves metrics for a Florm workspace. |

