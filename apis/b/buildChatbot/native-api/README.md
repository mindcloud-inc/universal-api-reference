# BuildChatbot: Native API Reference

A consolidated summary of BuildChatbot's API configuration and 28 documented operations, with links to official documentation.

- **Official docs:** https://documenter.getpostman.com/view/27680478/2s9YR6baAb
- **API base URL:** `https://api.buildchatbot.ai/api/v1`

## Authentication

### Bearer Token

Use a BuildChatbot bearer token obtained from the provider's non-OAuth login flow.

### Credentials

- **Bearer Token:** `token` · required · The BuildChatbot bearer token returned by the provider's login endpoint or captured from an authenticated session.

Send these headers with each API request:

```http
Authorization: Bearer <token>
```

[Official authentication documentation](https://documenter.getpostman.com/view/27680478/2s9YR6baAb)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (28 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create User Via Form](actions/create-user-via-form.md) | `POST /user/create/form` | [docs](https://documenter.getpostman.com/view/27680478/2s9YR6baAb#3758bf4a-67e9-412e-a2e8-63f57d152f33) |
| [Create User Via Magic Link](actions/create-user-via-magic-link.md) | `POST /user/create/magic_link` | [docs](https://documenter.getpostman.com/view/27680478/2s9YR6baAb#8691df55-0a0b-43b9-8318-aa453006ec5e) |
| [Forgot Password](actions/forgot-password.md) | `POST /forgot_password/` | [docs](https://documenter.getpostman.com/view/27680478/2s9YR6baAb#3a8a2ca3-d5e4-4d25-8a63-d2b2def4860e) |
| [Get Coupon Discount Percent](actions/get-coupon-discount-percent.md) | `GET /checkout/get/coupon/discount_percent/` | [docs](https://documenter.getpostman.com/view/27680478/2s9YR6baAb#27081964-7db7-421f-89b2-ada9a38d50ea) |
| [Get Current Subscription Plan](actions/get-current-subscription-plan.md) | `GET /user/current_subscription_plan` | [docs](https://documenter.getpostman.com/view/27680478/2s9YR6baAb#a6e3c554-4ad5-459e-baa0-264efc7d983a) |
| [Get Integrations Enable Detail](actions/get-integrations-enable-detail.md) | `GET /integrations/enable_details` | [docs](https://documenter.getpostman.com/view/27680478/2s9YR6baAb#180f9ce2-17b7-4f6c-9ad2-df29f0a4b94f) |
| [Get Slack Workspace Details](actions/get-slack-workspace-details.md) | `GET /slack/workspace_details/` | [docs](https://documenter.getpostman.com/view/27680478/2s9YR6baAb#3e30595f-a6fc-4771-bfd4-234506af006f) |
| [Get Subscription Plan Details](actions/get-subscription-plan-details.md) | `GET /checkout/subscription_plan_details/` | [docs](https://documenter.getpostman.com/view/27680478/2s9YR6baAb#a2e80a10-465f-488e-844e-d772a9f31f2d) |
| [Get Tenant Metrics](actions/get-tenant-metrics.md) | `GET /user/get_all_tenant_metrics` | [docs](https://documenter.getpostman.com/view/27680478/2s9YR6baAb#b8919ba4-8fc3-47c9-a106-f77bd7f4758a) |
| [Get Tenant Subscription Details](actions/get-tenant-subscription-details.md) | `GET /tenant/{{tenantId}}/subscription_details` | [docs](https://documenter.getpostman.com/view/27680478/2s9YR6baAb#14af84c7-5388-4eb8-ab54-936093e9f8e1) |
| [Get User Details](actions/get-user-details.md) | `GET /user/` | [docs](https://documenter.getpostman.com/view/27680478/2s9YR6baAb#507e5bce-d38c-4745-a315-a17c6bcb7982) |
| [Get User Profile Details](actions/get-user-profile-details.md) | `GET /profile_details/` | [docs](https://documenter.getpostman.com/view/27680478/2s9YR6baAb#e48aead1-ce9d-4fb5-8554-a557d3db9d8e) |
| [Get Zapier Enable Detail](actions/get-zapier-enable-detail.md) | `GET /zapier/enable_details` | [docs](https://documenter.getpostman.com/view/27680478/2s9YR6baAb#df3ffd2f-3ee7-4ddb-903b-fd8c99aae891) |
| [List Available Fonts](actions/list-available-fonts.md) | `GET /bot/fonts` | [docs](https://documenter.getpostman.com/view/27680478/2s9YR6baAb#a71ac1cf-135e-4961-a313-d6c597983f84) |
| [List Recent Chat History](actions/list-recent-chat-history.md) | `GET /bot/chat-history/recent/` | [docs](https://documenter.getpostman.com/view/27680478/2s9YR6baAb#77ffafb3-2474-4a73-9592-28320bce20f5) |
| [List Subscription Plan History](actions/list-subscription-plan-history.md) | `GET /user/subscription_plan_history` | [docs](https://documenter.getpostman.com/view/27680478/2s9YR6baAb#814dd9ed-cb44-410a-a167-dbab7fb33f57) |
| [List Subscription Plans](actions/list-subscription-plans.md) | `GET /subcriptionplans/monthly/rupee/` | [docs](https://documenter.getpostman.com/view/27680478/2s9YR6baAb#b5a68f08-118b-406f-94e3-221a4e248f5b) |
| [List Tenant Bots](actions/list-tenant-bots.md) | `GET /user/bots` | [docs](https://documenter.getpostman.com/view/27680478/2s9YR6baAb#cba9b7f0-980b-4daf-8d17-f07ca0997a49) |
| [List User Bots](actions/list-user-bots.md) | `GET /user/get_all_user_bots/` | [docs](https://documenter.getpostman.com/view/27680478/2s9YR6baAb#f4e7a568-2c20-480f-b306-caa7333be04f) |
| [List User Identifications](actions/list-user-identifications.md) | `GET /zapier/useridentification/list` | [docs](https://documenter.getpostman.com/view/27680478/2s9YR6baAb#71f8b43a-964c-4fa0-9a87-74632a16b446) |
| [Login](actions/login.md) | `POST /login` | [docs](https://documenter.getpostman.com/view/27680478/2s9YR6baAb#45b1b734-a65b-4975-ba30-9ce5646c8893) |
| [Logout](actions/logout.md) | `POST /logout` | [docs](https://documenter.getpostman.com/view/27680478/2s9YR6baAb#569c56b2-2ce6-4503-8424-9264ff3c57e7) |
| [Request Magic Link From And To Email](actions/request-magic-link-from-and-to-email.md) | `POST /login_with_magic_link_from_and_to_email` | [docs](https://documenter.getpostman.com/view/27680478/2s9YR6baAb#2781b6a8-c8d0-47fa-9b2f-bbc6dcbd3ff0) |
| [Request Magic Link Login](actions/request-magic-link-login.md) | `POST /login_with_magic_link` | [docs](https://documenter.getpostman.com/view/27680478/2s9YR6baAb#cbe7bef2-58c8-4e61-beec-4cbfb2d30bc0) |
| [Resend Verification Email](actions/resend-verification-email.md) | `POST /user/resend_verification_link/` | [docs](https://documenter.getpostman.com/view/27680478/2s9YR6baAb#a55531a5-e5ff-41c5-9f37-67b502f4e6ab) |
| [Reset Password](actions/reset-password.md) | `POST /password/reset//` | [docs](https://documenter.getpostman.com/view/27680478/2s9YR6baAb#b77c417f-873a-4285-bebb-6da9f314c658) |
| [Validate Selected Subscription Plan](actions/validate-selected-subscription-plan.md) | `GET /checkout/warning_for_sbscription_plan_upgrade/` | [docs](https://documenter.getpostman.com/view/27680478/2s9YR6baAb#93d1b08a-46c5-4606-96ff-e0b85f538635) |
| [Verify OTP](actions/verify-otp.md) | `POST /user/verify_otp` | [docs](https://documenter.getpostman.com/view/27680478/2s9YR6baAb#febd1d1b-8152-4db9-8111-c742271298a6) |
