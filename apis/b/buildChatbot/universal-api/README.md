# <img src="https://images.mindcloud.co/apps/icons/buildchatbot-icon-square_1775507499424.png" alt="BuildChatbot logo" width="28" height="28"> BuildChatbot: Universal API

BuildChatbot lets teams create, manage, and embed AI chatbots, bot content sources, chat history, live-chat handoff, tenant metrics, and integration settings through the provider's REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/buildChatbot/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 28
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://buildchatbot.ai/
- **Vendor API docs:** https://documenter.getpostman.com/view/27680478/2s9YR6baAb

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Tenant Bots](actions/list-tenant-bots.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buildChatbot/latest/actions/list-tenant-bots?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (28)

### Bot

| Action | Method | Description |
| --- | --- | --- |
| [List Tenant Bots](actions/list-tenant-bots.md) | GET | Retrieves tenant bot records from BuildChatbot. |
| [List User Bots](actions/list-user-bots.md) | GET | Retrieves user bot records from BuildChatbot. |

### Coupon Discount

| Action | Method | Description |
| --- | --- | --- |
| [Get Coupon Discount Percent](actions/get-coupon-discount-percent.md) | GET | Retrieves a coupon discount percent from BuildChatbot. |

### Font

| Action | Method | Description |
| --- | --- | --- |
| [List Available Fonts](actions/list-available-fonts.md) | GET | Retrieves available font options from BuildChatbot. |

### Integration Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get Integrations Enable Detail](actions/get-integrations-enable-detail.md) | GET | Retrieves integrations enable details from BuildChatbot. |

### Login Session

| Action | Method | Description |
| --- | --- | --- |
| [Login](actions/login.md) | POST | Creates a login session in BuildChatbot. |

### Magic Link Email Request

| Action | Method | Description |
| --- | --- | --- |
| [Request Magic Link From And To Email](actions/request-magic-link-from-and-to-email.md) | POST | Requests a magic link between email addresses in BuildChatbot. |

### Magic Link Login

| Action | Method | Description |
| --- | --- | --- |
| [Request Magic Link Login](actions/request-magic-link-login.md) | POST | Requests a magic link login from BuildChatbot. |

### Otp Verification

| Action | Method | Description |
| --- | --- | --- |
| [Verify OTP](actions/verify-otp.md) | POST | Verifies a one-time password in BuildChatbot. |

### Password Reset

| Action | Method | Description |
| --- | --- | --- |
| [Reset Password](actions/reset-password.md) | PUT | Updates a user password in BuildChatbot. |

### Password Reset Request

| Action | Method | Description |
| --- | --- | --- |
| [Forgot Password](actions/forgot-password.md) | POST | Requests a password reset from BuildChatbot. |

### Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get User Profile Details](actions/get-user-profile-details.md) | GET | Retrieves user profile details from BuildChatbot. |

### Recent Chat History

| Action | Method | Description |
| --- | --- | --- |
| [List Recent Chat History](actions/list-recent-chat-history.md) | GET | Retrieves recent chat history from BuildChatbot. |

### Session

| Action | Method | Description |
| --- | --- | --- |
| [Logout](actions/logout.md) | DELETE | Deletes the current session from BuildChatbot. |

### Slack Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Get Slack Workspace Details](actions/get-slack-workspace-details.md) | GET | Retrieves Slack workspace details from BuildChatbot. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Subscription Plan](actions/get-current-subscription-plan.md) | GET | Retrieves the current subscription plan from BuildChatbot. |

### Subscription History

| Action | Method | Description |
| --- | --- | --- |
| [List Subscription Plan History](actions/list-subscription-plan-history.md) | GET | Retrieves subscription plan history from BuildChatbot. |

### Subscription Plan

| Action | Method | Description |
| --- | --- | --- |
| [Get Subscription Plan Details](actions/get-subscription-plan-details.md) | GET | Retrieves subscription plan details from BuildChatbot. |
| [List Subscription Plans](actions/list-subscription-plans.md) | GET | Retrieves subscription plan options from BuildChatbot. |

### Subscription Upgrade Validation

| Action | Method | Description |
| --- | --- | --- |
| [Validate Selected Subscription Plan](actions/validate-selected-subscription-plan.md) | GET | Validates a selected subscription plan in BuildChatbot. |

### Tenant Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Get Tenant Metrics](actions/get-tenant-metrics.md) | GET | Retrieves tenant usage metrics from BuildChatbot. |

### Tenant Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Get Tenant Subscription Details](actions/get-tenant-subscription-details.md) | GET | Retrieves tenant subscription details from BuildChatbot. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create User Via Form](actions/create-user-via-form.md) | POST | Creates a user in BuildChatbot via form signup. |
| [Create User Via Magic Link](actions/create-user-via-magic-link.md) | POST | Creates a user in BuildChatbot via magic link. |
| [Get User Details](actions/get-user-details.md) | GET | Retrieves user account details from BuildChatbot. |

### User Identification

| Action | Method | Description |
| --- | --- | --- |
| [List User Identifications](actions/list-user-identifications.md) | GET | Retrieves user identification records from BuildChatbot. |

### Verification Email

| Action | Method | Description |
| --- | --- | --- |
| [Resend Verification Email](actions/resend-verification-email.md) | POST | Resends a verification email from BuildChatbot. |

### Zapier Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get Zapier Enable Detail](actions/get-zapier-enable-detail.md) | GET | Retrieves Zapier enable details from BuildChatbot. |

