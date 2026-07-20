# Florm: Native API Reference

A consolidated summary of Florm's API configuration and 27 documented operations, with links to official documentation.

- **Official docs:** https://api.florm.io/docs
- **OpenAPI specification:** https://api.florm.io/openapi.json
- **API base URL:** `https://api.florm.io`

## Authentication

### Bearer Token

Use a Florm access token for authenticated API requests. MindCloud sends it as the bearer token in the Authorization header.

### Credentials

- **Access Token:** `accessToken` · required · Florm bearer access token used for authenticated API calls.
- **Refresh Token:** `refreshToken` · optional · Optional Florm refresh token stored for continuity and manual token renewal.

Send these headers with each API request:

```http
Authorization: Bearer <accessToken>
Authorization: Bearer <refreshToken>
```

[Official authentication documentation](https://api.florm.io/docs)

## Endpoints (27 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Copy Form](actions/copy-form.md) | `POST /v1/forms/:form_guid/copy` | [docs](https://api.florm.io/docs#/default/copy_form_v1_forms__form_guid__copy_post) |
| [Create Form](actions/create-form.md) | `POST /v1/forms/` | [docs](https://api.florm.io/docs#/default/create_form_v1_forms__post) |
| [Create Magic Link](actions/create-magic-link.md) | `POST /v1/auth/magic-links` | [docs](https://api.florm.io/docs#/default/create_magic_link_v1_auth_magic_links_post) |
| [Delete Form](actions/delete-form.md) | `DELETE /v1/forms/:form_guid` | [docs](https://api.florm.io/docs#/default/delete_form_v1_forms__form_guid__delete) |
| [Export Form Analytics](actions/export-form-analytics.md) | `POST /v1/export/form/analytics` | [docs](https://api.florm.io/docs#/default/export_analytics_form_v1_export_form_analytics_post) |
| [Export Form Answers](actions/export-form-answers.md) | `POST /v1/export/form/answers` | [docs](https://api.florm.io/docs#/default/export_answers_form_v1_export_form_answers_post) |
| [Export Form Step Answers](actions/export-form-step-answers.md) | `POST /v1/export/form/step` | [docs](https://api.florm.io/docs#/default/export_answers_step_form_v1_export_form_step_post) |
| [Get Demo Token](actions/get-demo-token.md) | `PUT /v1/auth/magic-links/demo` | [docs](https://api.florm.io/docs#/default/get_demo_token_v1_auth_magic_links_demo_put) |
| [Get Export Task](actions/get-export-task.md) | `GET /v1/export/form/:form_guid/task/:task_guid` | [docs](https://api.florm.io/docs#/default/get_task_v1_export_form__form_guid__task__task_guid__get) |
| [Get Form](actions/get-form.md) | `GET /v1/forms/:form_guid` | [docs](https://api.florm.io/docs#/default/get_form_v1_forms__form_guid__get) |
| [Get Form Analytics](actions/get-form-analytics.md) | `POST /v1/analytics/form/:form_guid` | [docs](https://api.florm.io/docs#/default/form_analytics_v1_analytics_form__form_guid__post) |
| [Get Form Analytics Summary](actions/get-form-analytics-summary.md) | `POST /v1/analytics/form/:form_guid/summary` | [docs](https://api.florm.io/docs#/default/form_summary_v1_analytics_form__form_guid__summary_post) |
| [Get Form QR Code](actions/get-form-qr-code.md) | `GET /v1/forms/qrcode` | [docs](https://api.florm.io/docs#/default/get_qrcode_v1_forms_qrcode_get) |
| [Get Healthcheck](actions/get-healthcheck.md) | `GET /v1/healthcheck/` | [docs](https://api.florm.io/docs#/default/perform_healthcheck_v1_healthcheck__get) |
| [Get My Profile](actions/get-my-profile.md) | `GET /v1/auth/me` | [docs](https://api.florm.io/docs#/default/read_user_me_v1_auth_me_get) |
| [Get My Team](actions/get-my-team.md) | `GET /v1/teams/my` | [docs](https://api.florm.io/docs#/default/get_my_v1_teams_my_get) |
| [Get My Workspace](actions/get-my-workspace.md) | `GET /v1/workspaces/my` | [docs](https://api.florm.io/docs#/default/get_private_workspace_v1_workspaces_my_get) |
| [Get Workspace Metrics](actions/get-workspace-metrics.md) | `GET /v1/workspaces/:workspace_guid/metrics` | [docs](https://api.florm.io/docs#/default/get_workspaces_metrics_v1_workspaces__workspace_guid__metrics_get) |
| [List Form Answers](actions/list-form-answers.md) | `GET /v1/answers/form/:form_guid` | [docs](https://api.florm.io/docs#/default/form_answers_v1_answers_form__form_guid__get) |
| [List Form Step Answers](actions/list-form-step-answers.md) | `GET /v1/answers/form/:form_guid/step/:step_id` | [docs](https://api.florm.io/docs#/default/form_answers_step_v1_answers_form__form_guid__step__step_id__get) |
| [List Forms](actions/list-forms.md) | `GET /v1/forms/` | [docs](https://api.florm.io/docs#/default/get_all_forms_v1_forms__get) |
| [List Public Design Themes](actions/list-public-design-themes.md) | `GET /v1/design-themes/` | [docs](https://api.florm.io/docs#/default/get_all_public_v1_design_themes__get) |
| [Login With Magic Link](actions/login-with-magic-link.md) | `PUT /v1/auth/magic-links` | [docs](https://api.florm.io/docs#/default/login_magic_link_v1_auth_magic_links_put) |
| [Logout](actions/logout.md) | `DELETE /v1/auth/logout` | [docs](https://api.florm.io/docs#/default/logout_v1_auth_logout_delete) |
| [Refresh Access Token](actions/refresh-access-token.md) | `POST /v1/auth/refresh-token` | [docs](https://api.florm.io/docs#/default/refresh_token_v1_auth_refresh_token_post) |
| [Update Form](actions/update-form.md) | `POST /v1/forms/:form_guid` | [docs](https://api.florm.io/docs#/default/save_v1_forms__form_guid__post) |
| [Update My Profile](actions/update-my-profile.md) | `PUT /v1/auth/me` | [docs](https://api.florm.io/docs#/default/save_user_v1_auth_me_put) |
