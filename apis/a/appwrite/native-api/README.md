# Appwrite: Native API Reference

A consolidated summary of Appwrite's API configuration and 375 documented operations, with links to official documentation.

- **Official docs:** https://appwrite.io/docs/apis/rest
- **OpenAPI specification:** https://raw.githubusercontent.com/appwrite/appwrite/main/app/config/specs/open-api3-1.8.x-server.json
- **API base URL:** `https://cloud.appwrite.io/v1`

## Authentication

### Project API Key

Use an Appwrite project ID and Appwrite server API key for server REST requests.

### Credentials

- **Project ID:** `projectId` · required · Appwrite project ID used for the X-Appwrite-Project header.
- **API Key:** `apiKey` · required · Appwrite server API key used for the X-Appwrite-Key header.

Send these headers with each API request:

```http
X-Appwrite-Key: <apiKey>
X-Appwrite-Project: <projectId>
```

[Official authentication documentation](https://appwrite.io/docs/apis/rest)

## Endpoints (375 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create account](actions/account-create.md) | `POST /account` | [docs](https://appwrite.io/docs/references/cloud/server-rest/account) |
| [Create anonymous session](actions/account-create-anonymous-session.md) | `POST /account/sessions/anonymous` | [docs](https://appwrite.io/docs/references/cloud/server-rest/account) |
| [Create email password session](actions/account-create-email-password-session.md) | `POST /account/sessions/email` | [docs](https://appwrite.io/docs/references/cloud/server-rest/account) |
| [Create email token (OTP)](actions/account-create-email-token.md) | `POST /account/tokens/email` | [docs](https://appwrite.io/docs/references/cloud/server-rest/account) |
| [Create email verification](actions/account-create-email-verification.md) | `POST /account/verifications/email` | [docs](https://appwrite.io/docs/references/cloud/server-rest/account) |
| [Create JWT](actions/account-create-jwt.md) | `POST /account/jwts` | [docs](https://appwrite.io/docs/references/cloud/server-rest/account) |
| [Create magic URL token](actions/account-create-magic-urltoken.md) | `POST /account/tokens/magic-url` | [docs](https://appwrite.io/docs/references/cloud/server-rest/account) |
| [Create authenticator](actions/account-create-mfa-authenticator.md) | `POST /account/mfa/authenticators/{type}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/account) |
| [Create MFA challenge](actions/account-create-mfa-challenge.md) | `POST /account/mfa/challenges` | [docs](https://appwrite.io/docs/references/cloud/server-rest/account) |
| [Create MFA recovery codes](actions/account-create-mfa-recovery-codes.md) | `POST /account/mfa/recovery-codes` | [docs](https://appwrite.io/docs/references/cloud/server-rest/account) |
| [Create OAuth2 token](actions/account-create-oauth2-token.md) | `GET /account/tokens/oauth2/{provider}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/account) |
| [Create phone token](actions/account-create-phone-token.md) | `POST /account/tokens/phone` | [docs](https://appwrite.io/docs/references/cloud/server-rest/account) |
| [Create phone verification](actions/account-create-phone-verification.md) | `POST /account/verifications/phone` | [docs](https://appwrite.io/docs/references/cloud/server-rest/account) |
| [Create password recovery](actions/account-create-recovery.md) | `POST /account/recovery` | [docs](https://appwrite.io/docs/references/cloud/server-rest/account) |
| [Create session](actions/account-create-session.md) | `POST /account/sessions/token` | [docs](https://appwrite.io/docs/references/cloud/server-rest/account) |
| [Delete identity](actions/account-delete-identity.md) | `DELETE /account/identities/{identityId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/account) |
| [Delete authenticator](actions/account-delete-mfa-authenticator.md) | `DELETE /account/mfa/authenticators/{type}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/account) |
| [Delete session](actions/account-delete-session.md) | `DELETE /account/sessions/{sessionId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/account) |
| [Delete sessions](actions/account-delete-sessions.md) | `DELETE /account/sessions` | [docs](https://appwrite.io/docs/references/cloud/server-rest/account) |
| [Get account](actions/account-get.md) | `GET /account` | [docs](https://appwrite.io/docs/references/cloud/server-rest/account) |
| [List MFA recovery codes](actions/account-get-mfa-recovery-codes.md) | `GET /account/mfa/recovery-codes` | [docs](https://appwrite.io/docs/references/cloud/server-rest/account) |
| [Get account preferences](actions/account-get-prefs.md) | `GET /account/prefs` | [docs](https://appwrite.io/docs/references/cloud/server-rest/account) |
| [Get session](actions/account-get-session.md) | `GET /account/sessions/{sessionId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/account) |
| [List identities](actions/account-list-identities.md) | `GET /account/identities` | [docs](https://appwrite.io/docs/references/cloud/server-rest/account) |
| [List logs](actions/account-list-logs.md) | `GET /account/logs` | [docs](https://appwrite.io/docs/references/cloud/server-rest/account) |
| [List factors](actions/account-list-mfa-factors.md) | `GET /account/mfa/factors` | [docs](https://appwrite.io/docs/references/cloud/server-rest/account) |
| [List sessions](actions/account-list-sessions.md) | `GET /account/sessions` | [docs](https://appwrite.io/docs/references/cloud/server-rest/account) |
| [Update email](actions/account-update-email.md) | `PATCH /account/email` | [docs](https://appwrite.io/docs/references/cloud/server-rest/account) |
| [Update email verification (confirmation)](actions/account-update-email-verification.md) | `PUT /account/verifications/email` | [docs](https://appwrite.io/docs/references/cloud/server-rest/account) |
| [Update magic URL session](actions/account-update-magic-urlsession.md) | `PUT /account/sessions/magic-url` | [docs](https://appwrite.io/docs/references/cloud/server-rest/account) |
| [Update MFA](actions/account-update-mfa.md) | `PATCH /account/mfa` | [docs](https://appwrite.io/docs/references/cloud/server-rest/account) |
| [Update authenticator (confirmation)](actions/account-update-mfa-authenticator.md) | `PUT /account/mfa/authenticators/{type}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/account) |
| [Update MFA challenge (confirmation)](actions/account-update-mfa-challenge.md) | `PUT /account/mfa/challenges` | [docs](https://appwrite.io/docs/references/cloud/server-rest/account) |
| [Update MFA recovery codes (regenerate)](actions/account-update-mfa-recovery-codes.md) | `PATCH /account/mfa/recovery-codes` | [docs](https://appwrite.io/docs/references/cloud/server-rest/account) |
| [Update name](actions/account-update-name.md) | `PATCH /account/name` | [docs](https://appwrite.io/docs/references/cloud/server-rest/account) |
| [Update password](actions/account-update-password.md) | `PATCH /account/password` | [docs](https://appwrite.io/docs/references/cloud/server-rest/account) |
| [Update phone](actions/account-update-phone.md) | `PATCH /account/phone` | [docs](https://appwrite.io/docs/references/cloud/server-rest/account) |
| [Update phone session](actions/account-update-phone-session.md) | `PUT /account/sessions/phone` | [docs](https://appwrite.io/docs/references/cloud/server-rest/account) |
| [Update phone verification (confirmation)](actions/account-update-phone-verification.md) | `PUT /account/verifications/phone` | [docs](https://appwrite.io/docs/references/cloud/server-rest/account) |
| [Update preferences](actions/account-update-prefs.md) | `PATCH /account/prefs` | [docs](https://appwrite.io/docs/references/cloud/server-rest/account) |
| [Update password recovery (confirmation)](actions/account-update-recovery.md) | `PUT /account/recovery` | [docs](https://appwrite.io/docs/references/cloud/server-rest/account) |
| [Update session](actions/account-update-session.md) | `PATCH /account/sessions/{sessionId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/account) |
| [Update status](actions/account-update-status.md) | `PATCH /account/status` | [docs](https://appwrite.io/docs/references/cloud/server-rest/account) |
| [Get browser icon](actions/avatars-get-browser.md) | `GET /avatars/browsers/{code}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/avatars) |
| [Get credit card icon](actions/avatars-get-credit-card.md) | `GET /avatars/credit-cards/{code}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/avatars) |
| [Get favicon](actions/avatars-get-favicon.md) | `GET /avatars/favicon` | [docs](https://appwrite.io/docs/references/cloud/server-rest/avatars) |
| [Get country flag](actions/avatars-get-flag.md) | `GET /avatars/flags/{code}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/avatars) |
| [Get image from URL](actions/avatars-get-image.md) | `GET /avatars/image` | [docs](https://appwrite.io/docs/references/cloud/server-rest/avatars) |
| [Get user initials](actions/avatars-get-initials.md) | `GET /avatars/initials` | [docs](https://appwrite.io/docs/references/cloud/server-rest/avatars) |
| [Get QR code](actions/avatars-get-qr.md) | `GET /avatars/qr` | [docs](https://appwrite.io/docs/references/cloud/server-rest/avatars) |
| [Get webpage screenshot](actions/avatars-get-screenshot.md) | `GET /avatars/screenshots` | [docs](https://appwrite.io/docs/references/cloud/server-rest/avatars) |
| [Create database](actions/databases-create.md) | `POST /databases` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Create boolean attribute](actions/databases-create-boolean-attribute.md) | `POST /databases/{databaseId}/collections/{collectionId}/attributes/boolean` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Create collections](actions/databases-create-collection.md) | `POST /databases/{databaseId}/collections` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Create datetime attribute](actions/databases-create-datetime-attribute.md) | `POST /databases/{databaseId}/collections/{collectionId}/attributes/datetime` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Create document](actions/databases-create-document.md) | `POST /databases/{databaseId}/collections/{collectionId}/documents` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Create email attribute](actions/databases-create-email-attribute.md) | `POST /databases/{databaseId}/collections/{collectionId}/attributes/email` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Create enum attribute](actions/databases-create-enum-attribute.md) | `POST /databases/{databaseId}/collections/{collectionId}/attributes/enum` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Create float attribute](actions/databases-create-float-attribute.md) | `POST /databases/{databaseId}/collections/{collectionId}/attributes/float` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Create index](actions/databases-create-index.md) | `POST /databases/{databaseId}/collections/{collectionId}/indexes` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Create integer attribute](actions/databases-create-integer-attribute.md) | `POST /databases/{databaseId}/collections/{collectionId}/attributes/integer` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Create IP address attribute](actions/databases-create-ip-attribute.md) | `POST /databases/{databaseId}/collections/{collectionId}/attributes/ip` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Create line attribute](actions/databases-create-line-attribute.md) | `POST /databases/{databaseId}/collections/{collectionId}/attributes/line` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Create operations](actions/databases-create-operations.md) | `POST /databases/transactions/{transactionId}/operations` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Create point attribute](actions/databases-create-point-attribute.md) | `POST /databases/{databaseId}/collections/{collectionId}/attributes/point` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Create polygon attribute](actions/databases-create-polygon-attribute.md) | `POST /databases/{databaseId}/collections/{collectionId}/attributes/polygon` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Create relationship attribute](actions/databases-create-relationship-attribute.md) | `POST /databases/{databaseId}/collections/{collectionId}/attributes/relationship` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Create string attribute](actions/databases-create-string-attribute.md) | `POST /databases/{databaseId}/collections/{collectionId}/attributes/string` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Create transaction](actions/databases-create-transaction.md) | `POST /databases/transactions` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Create URL attribute](actions/databases-create-url-attribute.md) | `POST /databases/{databaseId}/collections/{collectionId}/attributes/url` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Decrement document attribute](actions/databases-decrement-document-attribute.md) | `PATCH /databases/{databaseId}/collections/{collectionId}/documents/{documentId}/{attribute}/decrement` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Delete database](actions/databases-delete.md) | `DELETE /databases/{databaseId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Delete attribute](actions/databases-delete-attribute.md) | `DELETE /databases/{databaseId}/collections/{collectionId}/attributes/{key}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Delete collection](actions/databases-delete-collection.md) | `DELETE /databases/{databaseId}/collections/{collectionId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Delete document](actions/databases-delete-document.md) | `DELETE /databases/{databaseId}/collections/{collectionId}/documents/{documentId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Delete documents](actions/databases-delete-documents.md) | `DELETE /databases/{databaseId}/collections/{collectionId}/documents` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Delete index](actions/databases-delete-index.md) | `DELETE /databases/{databaseId}/collections/{collectionId}/indexes/{key}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Delete transaction](actions/databases-delete-transaction.md) | `DELETE /databases/transactions/{transactionId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Get database](actions/databases-get.md) | `GET /databases/{databaseId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Get attribute](actions/databases-get-attribute.md) | `GET /databases/{databaseId}/collections/{collectionId}/attributes/{key}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Get collection](actions/databases-get-collection.md) | `GET /databases/{databaseId}/collections/{collectionId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Get document](actions/databases-get-document.md) | `GET /databases/{databaseId}/collections/{collectionId}/documents/{documentId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Get index](actions/databases-get-index.md) | `GET /databases/{databaseId}/collections/{collectionId}/indexes/{key}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Get transaction](actions/databases-get-transaction.md) | `GET /databases/transactions/{transactionId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Increment document attribute](actions/databases-increment-document-attribute.md) | `PATCH /databases/{databaseId}/collections/{collectionId}/documents/{documentId}/{attribute}/increment` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [List databases](actions/databases-list.md) | `GET /databases` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [List attributes](actions/databases-list-attributes.md) | `GET /databases/{databaseId}/collections/{collectionId}/attributes` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [List collections](actions/databases-list-collections.md) | `GET /databases/{databaseId}/collections` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [List documents](actions/databases-list-documents.md) | `GET /databases/{databaseId}/collections/{collectionId}/documents` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [List indexes](actions/databases-list-indexes.md) | `GET /databases/{databaseId}/collections/{collectionId}/indexes` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [List transactions](actions/databases-list-transactions.md) | `GET /databases/transactions` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Update database](actions/databases-update.md) | `PUT /databases/{databaseId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Update boolean attribute](actions/databases-update-boolean-attribute.md) | `PATCH /databases/{databaseId}/collections/{collectionId}/attributes/boolean/{key}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Update collection](actions/databases-update-collection.md) | `PUT /databases/{databaseId}/collections/{collectionId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Update datetime attribute](actions/databases-update-datetime-attribute.md) | `PATCH /databases/{databaseId}/collections/{collectionId}/attributes/datetime/{key}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Update document](actions/databases-update-document.md) | `PATCH /databases/{databaseId}/collections/{collectionId}/documents/{documentId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Update documents](actions/databases-update-documents.md) | `PATCH /databases/{databaseId}/collections/{collectionId}/documents` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Update email attribute](actions/databases-update-email-attribute.md) | `PATCH /databases/{databaseId}/collections/{collectionId}/attributes/email/{key}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Update enum attribute](actions/databases-update-enum-attribute.md) | `PATCH /databases/{databaseId}/collections/{collectionId}/attributes/enum/{key}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Update float attribute](actions/databases-update-float-attribute.md) | `PATCH /databases/{databaseId}/collections/{collectionId}/attributes/float/{key}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Update integer attribute](actions/databases-update-integer-attribute.md) | `PATCH /databases/{databaseId}/collections/{collectionId}/attributes/integer/{key}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Update IP address attribute](actions/databases-update-ip-attribute.md) | `PATCH /databases/{databaseId}/collections/{collectionId}/attributes/ip/{key}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Update line attribute](actions/databases-update-line-attribute.md) | `PATCH /databases/{databaseId}/collections/{collectionId}/attributes/line/{key}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Update point attribute](actions/databases-update-point-attribute.md) | `PATCH /databases/{databaseId}/collections/{collectionId}/attributes/point/{key}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Update polygon attribute](actions/databases-update-polygon-attribute.md) | `PATCH /databases/{databaseId}/collections/{collectionId}/attributes/polygon/{key}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Update relationship attribute](actions/databases-update-relationship-attribute.md) | `PATCH /databases/{databaseId}/collections/{collectionId}/attributes/{key}/relationship` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Update string attribute](actions/databases-update-string-attribute.md) | `PATCH /databases/{databaseId}/collections/{collectionId}/attributes/string/{key}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Update transaction](actions/databases-update-transaction.md) | `PATCH /databases/transactions/{transactionId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Update URL attribute](actions/databases-update-url-attribute.md) | `PATCH /databases/{databaseId}/collections/{collectionId}/attributes/url/{key}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Upsert a document](actions/databases-upsert-document.md) | `PUT /databases/{databaseId}/collections/{collectionId}/documents/{documentId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Upsert documents](actions/databases-upsert-documents.md) | `PUT /databases/{databaseId}/collections/{collectionId}/documents` | [docs](https://appwrite.io/docs/references/cloud/server-rest/databases) |
| [Create function](actions/functions-create.md) | `POST /functions` | [docs](https://appwrite.io/docs/references/cloud/server-rest/functions) |
| [Create deployment](actions/functions-create-deployment.md) | `POST /functions/{functionId}/deployments` | [docs](https://appwrite.io/docs/references/cloud/server-rest/functions) |
| [Create duplicate deployment](actions/functions-create-duplicate-deployment.md) | `POST /functions/{functionId}/deployments/duplicate` | [docs](https://appwrite.io/docs/references/cloud/server-rest/functions) |
| [Create execution](actions/functions-create-execution.md) | `POST /functions/{functionId}/executions` | [docs](https://appwrite.io/docs/references/cloud/server-rest/functions) |
| [Create template deployment](actions/functions-create-template-deployment.md) | `POST /functions/{functionId}/deployments/template` | [docs](https://appwrite.io/docs/references/cloud/server-rest/functions) |
| [Create variable](actions/functions-create-variable.md) | `POST /functions/{functionId}/variables` | [docs](https://appwrite.io/docs/references/cloud/server-rest/functions) |
| [Create VCS deployment](actions/functions-create-vcs-deployment.md) | `POST /functions/{functionId}/deployments/vcs` | [docs](https://appwrite.io/docs/references/cloud/server-rest/functions) |
| [Delete function](actions/functions-delete.md) | `DELETE /functions/{functionId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/functions) |
| [Delete deployment](actions/functions-delete-deployment.md) | `DELETE /functions/{functionId}/deployments/{deploymentId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/functions) |
| [Delete execution](actions/functions-delete-execution.md) | `DELETE /functions/{functionId}/executions/{executionId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/functions) |
| [Delete variable](actions/functions-delete-variable.md) | `DELETE /functions/{functionId}/variables/{variableId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/functions) |
| [Get function](actions/functions-get.md) | `GET /functions/{functionId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/functions) |
| [Get deployment](actions/functions-get-deployment.md) | `GET /functions/{functionId}/deployments/{deploymentId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/functions) |
| [Get deployment download](actions/functions-get-deployment-download.md) | `GET /functions/{functionId}/deployments/{deploymentId}/download` | [docs](https://appwrite.io/docs/references/cloud/server-rest/functions) |
| [Get execution](actions/functions-get-execution.md) | `GET /functions/{functionId}/executions/{executionId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/functions) |
| [Get variable](actions/functions-get-variable.md) | `GET /functions/{functionId}/variables/{variableId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/functions) |
| [List functions](actions/functions-list.md) | `GET /functions` | [docs](https://appwrite.io/docs/references/cloud/server-rest/functions) |
| [List deployments](actions/functions-list-deployments.md) | `GET /functions/{functionId}/deployments` | [docs](https://appwrite.io/docs/references/cloud/server-rest/functions) |
| [List executions](actions/functions-list-executions.md) | `GET /functions/{functionId}/executions` | [docs](https://appwrite.io/docs/references/cloud/server-rest/functions) |
| [List runtimes](actions/functions-list-runtimes.md) | `GET /functions/runtimes` | [docs](https://appwrite.io/docs/references/cloud/server-rest/functions) |
| [List specifications](actions/functions-list-specifications.md) | `GET /functions/specifications` | [docs](https://appwrite.io/docs/references/cloud/server-rest/functions) |
| [List variables](actions/functions-list-variables.md) | `GET /functions/{functionId}/variables` | [docs](https://appwrite.io/docs/references/cloud/server-rest/functions) |
| [Update function](actions/functions-update.md) | `PUT /functions/{functionId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/functions) |
| [Update deployment status](actions/functions-update-deployment-status.md) | `PATCH /functions/{functionId}/deployments/{deploymentId}/status` | [docs](https://appwrite.io/docs/references/cloud/server-rest/functions) |
| [Update function's deployment](actions/functions-update-function-deployment.md) | `PATCH /functions/{functionId}/deployment` | [docs](https://appwrite.io/docs/references/cloud/server-rest/functions) |
| [Update variable](actions/functions-update-variable.md) | `PUT /functions/{functionId}/variables/{variableId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/functions) |
| [GraphQL endpoint](actions/graphql-mutation.md) | `POST /graphql/mutation` | [docs](https://appwrite.io/docs/references/cloud/server-rest/graphql) |
| [GraphQL endpoint](actions/graphql-query.md) | `POST /graphql` | [docs](https://appwrite.io/docs/references/cloud/server-rest/graphql) |
| [Get HTTP](actions/health-get.md) | `GET /health` | [docs](https://appwrite.io/docs/references/cloud/server-rest/health) |
| [Get antivirus](actions/health-get-antivirus.md) | `GET /health/anti-virus` | [docs](https://appwrite.io/docs/references/cloud/server-rest/health) |
| [Get cache](actions/health-get-cache.md) | `GET /health/cache` | [docs](https://appwrite.io/docs/references/cloud/server-rest/health) |
| [Get the SSL certificate for a domain](actions/health-get-certificate.md) | `GET /health/certificate` | [docs](https://appwrite.io/docs/references/cloud/server-rest/health) |
| [Get DB](actions/health-get-db.md) | `GET /health/db` | [docs](https://appwrite.io/docs/references/cloud/server-rest/health) |
| [Get number of failed queue jobs](actions/health-get-failed-jobs.md) | `GET /health/queue/failed/{name}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/health) |
| [Get pubsub](actions/health-get-pub-sub.md) | `GET /health/pubsub` | [docs](https://appwrite.io/docs/references/cloud/server-rest/health) |
| [Get builds queue](actions/health-get-queue-builds.md) | `GET /health/queue/builds` | [docs](https://appwrite.io/docs/references/cloud/server-rest/health) |
| [Get certificates queue](actions/health-get-queue-certificates.md) | `GET /health/queue/certificates` | [docs](https://appwrite.io/docs/references/cloud/server-rest/health) |
| [Get databases queue](actions/health-get-queue-databases.md) | `GET /health/queue/databases` | [docs](https://appwrite.io/docs/references/cloud/server-rest/health) |
| [Get deletes queue](actions/health-get-queue-deletes.md) | `GET /health/queue/deletes` | [docs](https://appwrite.io/docs/references/cloud/server-rest/health) |
| [Get functions queue](actions/health-get-queue-functions.md) | `GET /health/queue/functions` | [docs](https://appwrite.io/docs/references/cloud/server-rest/health) |
| [Get logs queue](actions/health-get-queue-logs.md) | `GET /health/queue/logs` | [docs](https://appwrite.io/docs/references/cloud/server-rest/health) |
| [Get mails queue](actions/health-get-queue-mails.md) | `GET /health/queue/mails` | [docs](https://appwrite.io/docs/references/cloud/server-rest/health) |
| [Get messaging queue](actions/health-get-queue-messaging.md) | `GET /health/queue/messaging` | [docs](https://appwrite.io/docs/references/cloud/server-rest/health) |
| [Get migrations queue](actions/health-get-queue-migrations.md) | `GET /health/queue/migrations` | [docs](https://appwrite.io/docs/references/cloud/server-rest/health) |
| [Get stats resources queue](actions/health-get-queue-stats-resources.md) | `GET /health/queue/stats-resources` | [docs](https://appwrite.io/docs/references/cloud/server-rest/health) |
| [Get stats usage queue](actions/health-get-queue-usage.md) | `GET /health/queue/stats-usage` | [docs](https://appwrite.io/docs/references/cloud/server-rest/health) |
| [Get webhooks queue](actions/health-get-queue-webhooks.md) | `GET /health/queue/webhooks` | [docs](https://appwrite.io/docs/references/cloud/server-rest/health) |
| [Get storage](actions/health-get-storage.md) | `GET /health/storage` | [docs](https://appwrite.io/docs/references/cloud/server-rest/health) |
| [Get local storage](actions/health-get-storage-local.md) | `GET /health/storage/local` | [docs](https://appwrite.io/docs/references/cloud/server-rest/health) |
| [Get time](actions/health-get-time.md) | `GET /health/time` | [docs](https://appwrite.io/docs/references/cloud/server-rest/health) |
| [Get user locale](actions/locale-get.md) | `GET /locale` | [docs](https://appwrite.io/docs/references/cloud/server-rest/locale) |
| [List locale codes](actions/locale-list-codes.md) | `GET /locale/codes` | [docs](https://appwrite.io/docs/references/cloud/server-rest/locale) |
| [List continents](actions/locale-list-continents.md) | `GET /locale/continents` | [docs](https://appwrite.io/docs/references/cloud/server-rest/locale) |
| [List countries](actions/locale-list-countries.md) | `GET /locale/countries` | [docs](https://appwrite.io/docs/references/cloud/server-rest/locale) |
| [List EU countries](actions/locale-list-countries-eu.md) | `GET /locale/countries/eu` | [docs](https://appwrite.io/docs/references/cloud/server-rest/locale) |
| [List countries phone codes](actions/locale-list-countries-phones.md) | `GET /locale/countries/phones` | [docs](https://appwrite.io/docs/references/cloud/server-rest/locale) |
| [List currencies](actions/locale-list-currencies.md) | `GET /locale/currencies` | [docs](https://appwrite.io/docs/references/cloud/server-rest/locale) |
| [List languages](actions/locale-list-languages.md) | `GET /locale/languages` | [docs](https://appwrite.io/docs/references/cloud/server-rest/locale) |
| [Create APNS provider](actions/messaging-create-apns-provider.md) | `POST /messaging/providers/apns` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [Create email](actions/messaging-create-email.md) | `POST /messaging/messages/email` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [Create FCM provider](actions/messaging-create-fcm-provider.md) | `POST /messaging/providers/fcm` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [Create Mailgun provider](actions/messaging-create-mailgun-provider.md) | `POST /messaging/providers/mailgun` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [Create Msg91 provider](actions/messaging-create-msg91-provider.md) | `POST /messaging/providers/msg91` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [Create push notification](actions/messaging-create-push.md) | `POST /messaging/messages/push` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [Create Resend provider](actions/messaging-create-resend-provider.md) | `POST /messaging/providers/resend` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [Create Sendgrid provider](actions/messaging-create-sendgrid-provider.md) | `POST /messaging/providers/sendgrid` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [Create SMS](actions/messaging-create-sms.md) | `POST /messaging/messages/sms` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [Create SMTP provider](actions/messaging-create-smtp-provider.md) | `POST /messaging/providers/smtp` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [Create subscriber](actions/messaging-create-subscriber.md) | `POST /messaging/topics/{topicId}/subscribers` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [Create Telesign provider](actions/messaging-create-telesign-provider.md) | `POST /messaging/providers/telesign` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [Create Textmagic provider](actions/messaging-create-textmagic-provider.md) | `POST /messaging/providers/textmagic` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [Create topic](actions/messaging-create-topic.md) | `POST /messaging/topics` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [Create Twilio provider](actions/messaging-create-twilio-provider.md) | `POST /messaging/providers/twilio` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [Create Vonage provider](actions/messaging-create-vonage-provider.md) | `POST /messaging/providers/vonage` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [Delete message](actions/messaging-delete.md) | `DELETE /messaging/messages/{messageId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [Delete provider](actions/messaging-delete-provider.md) | `DELETE /messaging/providers/{providerId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [Delete subscriber](actions/messaging-delete-subscriber.md) | `DELETE /messaging/topics/{topicId}/subscribers/{subscriberId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [Delete topic](actions/messaging-delete-topic.md) | `DELETE /messaging/topics/{topicId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [Get message](actions/messaging-get-message.md) | `GET /messaging/messages/{messageId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [Get provider](actions/messaging-get-provider.md) | `GET /messaging/providers/{providerId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [Get subscriber](actions/messaging-get-subscriber.md) | `GET /messaging/topics/{topicId}/subscribers/{subscriberId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [Get topic](actions/messaging-get-topic.md) | `GET /messaging/topics/{topicId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [List message logs](actions/messaging-list-message-logs.md) | `GET /messaging/messages/{messageId}/logs` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [List messages](actions/messaging-list-messages.md) | `GET /messaging/messages` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [List provider logs](actions/messaging-list-provider-logs.md) | `GET /messaging/providers/{providerId}/logs` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [List providers](actions/messaging-list-providers.md) | `GET /messaging/providers` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [List subscriber logs](actions/messaging-list-subscriber-logs.md) | `GET /messaging/subscribers/{subscriberId}/logs` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [List subscribers](actions/messaging-list-subscribers.md) | `GET /messaging/topics/{topicId}/subscribers` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [List message targets](actions/messaging-list-targets.md) | `GET /messaging/messages/{messageId}/targets` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [List topic logs](actions/messaging-list-topic-logs.md) | `GET /messaging/topics/{topicId}/logs` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [List topics](actions/messaging-list-topics.md) | `GET /messaging/topics` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [Update APNS provider](actions/messaging-update-apns-provider.md) | `PATCH /messaging/providers/apns/{providerId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [Update email](actions/messaging-update-email.md) | `PATCH /messaging/messages/email/{messageId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [Update FCM provider](actions/messaging-update-fcm-provider.md) | `PATCH /messaging/providers/fcm/{providerId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [Update Mailgun provider](actions/messaging-update-mailgun-provider.md) | `PATCH /messaging/providers/mailgun/{providerId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [Update Msg91 provider](actions/messaging-update-msg91-provider.md) | `PATCH /messaging/providers/msg91/{providerId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [Update push notification](actions/messaging-update-push.md) | `PATCH /messaging/messages/push/{messageId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [Update Resend provider](actions/messaging-update-resend-provider.md) | `PATCH /messaging/providers/resend/{providerId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [Update Sendgrid provider](actions/messaging-update-sendgrid-provider.md) | `PATCH /messaging/providers/sendgrid/{providerId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [Update SMS](actions/messaging-update-sms.md) | `PATCH /messaging/messages/sms/{messageId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [Update SMTP provider](actions/messaging-update-smtp-provider.md) | `PATCH /messaging/providers/smtp/{providerId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [Update Telesign provider](actions/messaging-update-telesign-provider.md) | `PATCH /messaging/providers/telesign/{providerId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [Update Textmagic provider](actions/messaging-update-textmagic-provider.md) | `PATCH /messaging/providers/textmagic/{providerId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [Update topic](actions/messaging-update-topic.md) | `PATCH /messaging/topics/{topicId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [Update Twilio provider](actions/messaging-update-twilio-provider.md) | `PATCH /messaging/providers/twilio/{providerId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [Update Vonage provider](actions/messaging-update-vonage-provider.md) | `PATCH /messaging/providers/vonage/{providerId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/messaging) |
| [Create site](actions/sites-create.md) | `POST /sites` | [docs](https://appwrite.io/docs/references/cloud/server-rest/sites) |
| [Create deployment](actions/sites-create-deployment.md) | `POST /sites/{siteId}/deployments` | [docs](https://appwrite.io/docs/references/cloud/server-rest/sites) |
| [Create duplicate deployment](actions/sites-create-duplicate-deployment.md) | `POST /sites/{siteId}/deployments/duplicate` | [docs](https://appwrite.io/docs/references/cloud/server-rest/sites) |
| [Create template deployment](actions/sites-create-template-deployment.md) | `POST /sites/{siteId}/deployments/template` | [docs](https://appwrite.io/docs/references/cloud/server-rest/sites) |
| [Create variable](actions/sites-create-variable.md) | `POST /sites/{siteId}/variables` | [docs](https://appwrite.io/docs/references/cloud/server-rest/sites) |
| [Create VCS deployment](actions/sites-create-vcs-deployment.md) | `POST /sites/{siteId}/deployments/vcs` | [docs](https://appwrite.io/docs/references/cloud/server-rest/sites) |
| [Delete site](actions/sites-delete.md) | `DELETE /sites/{siteId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/sites) |
| [Delete deployment](actions/sites-delete-deployment.md) | `DELETE /sites/{siteId}/deployments/{deploymentId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/sites) |
| [Delete log](actions/sites-delete-log.md) | `DELETE /sites/{siteId}/logs/{logId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/sites) |
| [Delete variable](actions/sites-delete-variable.md) | `DELETE /sites/{siteId}/variables/{variableId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/sites) |
| [Get site](actions/sites-get.md) | `GET /sites/{siteId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/sites) |
| [Get deployment](actions/sites-get-deployment.md) | `GET /sites/{siteId}/deployments/{deploymentId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/sites) |
| [Get deployment download](actions/sites-get-deployment-download.md) | `GET /sites/{siteId}/deployments/{deploymentId}/download` | [docs](https://appwrite.io/docs/references/cloud/server-rest/sites) |
| [Get log](actions/sites-get-log.md) | `GET /sites/{siteId}/logs/{logId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/sites) |
| [Get variable](actions/sites-get-variable.md) | `GET /sites/{siteId}/variables/{variableId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/sites) |
| [List sites](actions/sites-list.md) | `GET /sites` | [docs](https://appwrite.io/docs/references/cloud/server-rest/sites) |
| [List deployments](actions/sites-list-deployments.md) | `GET /sites/{siteId}/deployments` | [docs](https://appwrite.io/docs/references/cloud/server-rest/sites) |
| [List frameworks](actions/sites-list-frameworks.md) | `GET /sites/frameworks` | [docs](https://appwrite.io/docs/references/cloud/server-rest/sites) |
| [List logs](actions/sites-list-logs.md) | `GET /sites/{siteId}/logs` | [docs](https://appwrite.io/docs/references/cloud/server-rest/sites) |
| [List specifications](actions/sites-list-specifications.md) | `GET /sites/specifications` | [docs](https://appwrite.io/docs/references/cloud/server-rest/sites) |
| [List variables](actions/sites-list-variables.md) | `GET /sites/{siteId}/variables` | [docs](https://appwrite.io/docs/references/cloud/server-rest/sites) |
| [Update site](actions/sites-update.md) | `PUT /sites/{siteId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/sites) |
| [Update deployment status](actions/sites-update-deployment-status.md) | `PATCH /sites/{siteId}/deployments/{deploymentId}/status` | [docs](https://appwrite.io/docs/references/cloud/server-rest/sites) |
| [Update site's deployment](actions/sites-update-site-deployment.md) | `PATCH /sites/{siteId}/deployment` | [docs](https://appwrite.io/docs/references/cloud/server-rest/sites) |
| [Update variable](actions/sites-update-variable.md) | `PUT /sites/{siteId}/variables/{variableId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/sites) |
| [Create bucket](actions/storage-create-bucket.md) | `POST /storage/buckets` | [docs](https://appwrite.io/docs/references/cloud/server-rest/storage) |
| [Create file](actions/storage-create-file.md) | `POST /storage/buckets/{bucketId}/files` | [docs](https://appwrite.io/docs/references/cloud/server-rest/storage) |
| [Delete bucket](actions/storage-delete-bucket.md) | `DELETE /storage/buckets/{bucketId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/storage) |
| [Delete file](actions/storage-delete-file.md) | `DELETE /storage/buckets/{bucketId}/files/{fileId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/storage) |
| [Get bucket](actions/storage-get-bucket.md) | `GET /storage/buckets/{bucketId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/storage) |
| [Get file](actions/storage-get-file.md) | `GET /storage/buckets/{bucketId}/files/{fileId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/storage) |
| [Get file for download](actions/storage-get-file-download.md) | `GET /storage/buckets/{bucketId}/files/{fileId}/download` | [docs](https://appwrite.io/docs/references/cloud/server-rest/storage) |
| [Get file preview](actions/storage-get-file-preview.md) | `GET /storage/buckets/{bucketId}/files/{fileId}/preview` | [docs](https://appwrite.io/docs/references/cloud/server-rest/storage) |
| [Get file for view](actions/storage-get-file-view.md) | `GET /storage/buckets/{bucketId}/files/{fileId}/view` | [docs](https://appwrite.io/docs/references/cloud/server-rest/storage) |
| [List buckets](actions/storage-list-buckets.md) | `GET /storage/buckets` | [docs](https://appwrite.io/docs/references/cloud/server-rest/storage) |
| [List files](actions/storage-list-files.md) | `GET /storage/buckets/{bucketId}/files` | [docs](https://appwrite.io/docs/references/cloud/server-rest/storage) |
| [Update bucket](actions/storage-update-bucket.md) | `PUT /storage/buckets/{bucketId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/storage) |
| [Update file](actions/storage-update-file.md) | `PUT /storage/buckets/{bucketId}/files/{fileId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/storage) |
| [Create database](actions/tables-dbcreate.md) | `POST /tablesdb` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Create boolean column](actions/tables-dbcreate-boolean-column.md) | `POST /tablesdb/{databaseId}/tables/{tableId}/columns/boolean` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Create datetime column](actions/tables-dbcreate-datetime-column.md) | `POST /tablesdb/{databaseId}/tables/{tableId}/columns/datetime` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Create email column](actions/tables-dbcreate-email-column.md) | `POST /tablesdb/{databaseId}/tables/{tableId}/columns/email` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Create enum column](actions/tables-dbcreate-enum-column.md) | `POST /tablesdb/{databaseId}/tables/{tableId}/columns/enum` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Create float column](actions/tables-dbcreate-float-column.md) | `POST /tablesdb/{databaseId}/tables/{tableId}/columns/float` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Create index](actions/tables-dbcreate-index.md) | `POST /tablesdb/{databaseId}/tables/{tableId}/indexes` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Create integer column](actions/tables-dbcreate-integer-column.md) | `POST /tablesdb/{databaseId}/tables/{tableId}/columns/integer` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Create IP address column](actions/tables-dbcreate-ip-column.md) | `POST /tablesdb/{databaseId}/tables/{tableId}/columns/ip` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Create line column](actions/tables-dbcreate-line-column.md) | `POST /tablesdb/{databaseId}/tables/{tableId}/columns/line` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Create operations](actions/tables-dbcreate-operations.md) | `POST /tablesdb/transactions/{transactionId}/operations` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Create point column](actions/tables-dbcreate-point-column.md) | `POST /tablesdb/{databaseId}/tables/{tableId}/columns/point` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Create polygon column](actions/tables-dbcreate-polygon-column.md) | `POST /tablesdb/{databaseId}/tables/{tableId}/columns/polygon` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Create relationship column](actions/tables-dbcreate-relationship-column.md) | `POST /tablesdb/{databaseId}/tables/{tableId}/columns/relationship` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Create row](actions/tables-dbcreate-row.md) | `POST /tablesdb/{databaseId}/tables/{tableId}/rows` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Create string column](actions/tables-dbcreate-string-column.md) | `POST /tablesdb/{databaseId}/tables/{tableId}/columns/string` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Create table](actions/tables-dbcreate-table.md) | `POST /tablesdb/{databaseId}/tables` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Create transaction](actions/tables-dbcreate-transaction.md) | `POST /tablesdb/transactions` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Create URL column](actions/tables-dbcreate-url-column.md) | `POST /tablesdb/{databaseId}/tables/{tableId}/columns/url` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Decrement row column](actions/tables-dbdecrement-row-column.md) | `PATCH /tablesdb/{databaseId}/tables/{tableId}/rows/{rowId}/{column}/decrement` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Delete database](actions/tables-dbdelete.md) | `DELETE /tablesdb/{databaseId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Delete column](actions/tables-dbdelete-column.md) | `DELETE /tablesdb/{databaseId}/tables/{tableId}/columns/{key}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Delete index](actions/tables-dbdelete-index.md) | `DELETE /tablesdb/{databaseId}/tables/{tableId}/indexes/{key}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Delete row](actions/tables-dbdelete-row.md) | `DELETE /tablesdb/{databaseId}/tables/{tableId}/rows/{rowId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Delete rows](actions/tables-dbdelete-rows.md) | `DELETE /tablesdb/{databaseId}/tables/{tableId}/rows` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Delete table](actions/tables-dbdelete-table.md) | `DELETE /tablesdb/{databaseId}/tables/{tableId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Delete transaction](actions/tables-dbdelete-transaction.md) | `DELETE /tablesdb/transactions/{transactionId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Get database](actions/tables-dbget.md) | `GET /tablesdb/{databaseId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Get column](actions/tables-dbget-column.md) | `GET /tablesdb/{databaseId}/tables/{tableId}/columns/{key}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Get index](actions/tables-dbget-index.md) | `GET /tablesdb/{databaseId}/tables/{tableId}/indexes/{key}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Get row](actions/tables-dbget-row.md) | `GET /tablesdb/{databaseId}/tables/{tableId}/rows/{rowId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Get table](actions/tables-dbget-table.md) | `GET /tablesdb/{databaseId}/tables/{tableId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Get transaction](actions/tables-dbget-transaction.md) | `GET /tablesdb/transactions/{transactionId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Increment row column](actions/tables-dbincrement-row-column.md) | `PATCH /tablesdb/{databaseId}/tables/{tableId}/rows/{rowId}/{column}/increment` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [List databases](actions/tables-dblist.md) | `GET /tablesdb` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [List columns](actions/tables-dblist-columns.md) | `GET /tablesdb/{databaseId}/tables/{tableId}/columns` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [List indexes](actions/tables-dblist-indexes.md) | `GET /tablesdb/{databaseId}/tables/{tableId}/indexes` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [List rows](actions/tables-dblist-rows.md) | `GET /tablesdb/{databaseId}/tables/{tableId}/rows` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [List tables](actions/tables-dblist-tables.md) | `GET /tablesdb/{databaseId}/tables` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [List transactions](actions/tables-dblist-transactions.md) | `GET /tablesdb/transactions` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Update database](actions/tables-dbupdate.md) | `PUT /tablesdb/{databaseId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Update boolean column](actions/tables-dbupdate-boolean-column.md) | `PATCH /tablesdb/{databaseId}/tables/{tableId}/columns/boolean/{key}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Update dateTime column](actions/tables-dbupdate-datetime-column.md) | `PATCH /tablesdb/{databaseId}/tables/{tableId}/columns/datetime/{key}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Update email column](actions/tables-dbupdate-email-column.md) | `PATCH /tablesdb/{databaseId}/tables/{tableId}/columns/email/{key}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Update enum column](actions/tables-dbupdate-enum-column.md) | `PATCH /tablesdb/{databaseId}/tables/{tableId}/columns/enum/{key}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Update float column](actions/tables-dbupdate-float-column.md) | `PATCH /tablesdb/{databaseId}/tables/{tableId}/columns/float/{key}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Update integer column](actions/tables-dbupdate-integer-column.md) | `PATCH /tablesdb/{databaseId}/tables/{tableId}/columns/integer/{key}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Update IP address column](actions/tables-dbupdate-ip-column.md) | `PATCH /tablesdb/{databaseId}/tables/{tableId}/columns/ip/{key}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Update line column](actions/tables-dbupdate-line-column.md) | `PATCH /tablesdb/{databaseId}/tables/{tableId}/columns/line/{key}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Update point column](actions/tables-dbupdate-point-column.md) | `PATCH /tablesdb/{databaseId}/tables/{tableId}/columns/point/{key}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Update polygon column](actions/tables-dbupdate-polygon-column.md) | `PATCH /tablesdb/{databaseId}/tables/{tableId}/columns/polygon/{key}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Update relationship column](actions/tables-dbupdate-relationship-column.md) | `PATCH /tablesdb/{databaseId}/tables/{tableId}/columns/{key}/relationship` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Update row](actions/tables-dbupdate-row.md) | `PATCH /tablesdb/{databaseId}/tables/{tableId}/rows/{rowId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Update rows](actions/tables-dbupdate-rows.md) | `PATCH /tablesdb/{databaseId}/tables/{tableId}/rows` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Update string column](actions/tables-dbupdate-string-column.md) | `PATCH /tablesdb/{databaseId}/tables/{tableId}/columns/string/{key}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Update table](actions/tables-dbupdate-table.md) | `PUT /tablesdb/{databaseId}/tables/{tableId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Update transaction](actions/tables-dbupdate-transaction.md) | `PATCH /tablesdb/transactions/{transactionId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Update URL column](actions/tables-dbupdate-url-column.md) | `PATCH /tablesdb/{databaseId}/tables/{tableId}/columns/url/{key}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Upsert a row](actions/tables-dbupsert-row.md) | `PUT /tablesdb/{databaseId}/tables/{tableId}/rows/{rowId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Upsert rows](actions/tables-dbupsert-rows.md) | `PUT /tablesdb/{databaseId}/tables/{tableId}/rows` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tablesdb) |
| [Create team](actions/teams-create.md) | `POST /teams` | [docs](https://appwrite.io/docs/references/cloud/server-rest/teams) |
| [Create team membership](actions/teams-create-membership.md) | `POST /teams/{teamId}/memberships` | [docs](https://appwrite.io/docs/references/cloud/server-rest/teams) |
| [Delete team](actions/teams-delete.md) | `DELETE /teams/{teamId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/teams) |
| [Delete team membership](actions/teams-delete-membership.md) | `DELETE /teams/{teamId}/memberships/{membershipId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/teams) |
| [Get team](actions/teams-get.md) | `GET /teams/{teamId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/teams) |
| [Get team membership](actions/teams-get-membership.md) | `GET /teams/{teamId}/memberships/{membershipId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/teams) |
| [Get team preferences](actions/teams-get-prefs.md) | `GET /teams/{teamId}/prefs` | [docs](https://appwrite.io/docs/references/cloud/server-rest/teams) |
| [List teams](actions/teams-list.md) | `GET /teams` | [docs](https://appwrite.io/docs/references/cloud/server-rest/teams) |
| [List team memberships](actions/teams-list-memberships.md) | `GET /teams/{teamId}/memberships` | [docs](https://appwrite.io/docs/references/cloud/server-rest/teams) |
| [Update membership](actions/teams-update-membership.md) | `PATCH /teams/{teamId}/memberships/{membershipId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/teams) |
| [Update team membership status](actions/teams-update-membership-status.md) | `PATCH /teams/{teamId}/memberships/{membershipId}/status` | [docs](https://appwrite.io/docs/references/cloud/server-rest/teams) |
| [Update name](actions/teams-update-name.md) | `PUT /teams/{teamId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/teams) |
| [Update preferences](actions/teams-update-prefs.md) | `PUT /teams/{teamId}/prefs` | [docs](https://appwrite.io/docs/references/cloud/server-rest/teams) |
| [Create file token](actions/tokens-create-file-token.md) | `POST /tokens/buckets/{bucketId}/files/{fileId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tokens) |
| [Delete token](actions/tokens-delete.md) | `DELETE /tokens/{tokenId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tokens) |
| [Get token](actions/tokens-get.md) | `GET /tokens/{tokenId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tokens) |
| [List tokens](actions/tokens-list.md) | `GET /tokens/buckets/{bucketId}/files/{fileId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tokens) |
| [Update token](actions/tokens-update.md) | `PATCH /tokens/{tokenId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/tokens) |
| [Create user](actions/users-create.md) | `POST /users` | [docs](https://appwrite.io/docs/references/cloud/server-rest/users) |
| [Create user with Argon2 password](actions/users-create-argon2-user.md) | `POST /users/argon2` | [docs](https://appwrite.io/docs/references/cloud/server-rest/users) |
| [Create user with bcrypt password](actions/users-create-bcrypt-user.md) | `POST /users/bcrypt` | [docs](https://appwrite.io/docs/references/cloud/server-rest/users) |
| [Create user JWT](actions/users-create-jwt.md) | `POST /users/{userId}/jwts` | [docs](https://appwrite.io/docs/references/cloud/server-rest/users) |
| [Create user with MD5 password](actions/users-create-md5-user.md) | `POST /users/md5` | [docs](https://appwrite.io/docs/references/cloud/server-rest/users) |
| [Create MFA recovery codes](actions/users-create-mfa-recovery-codes.md) | `PATCH /users/{userId}/mfa/recovery-codes` | [docs](https://appwrite.io/docs/references/cloud/server-rest/users) |
| [Create user with PHPass password](actions/users-create-phpass-user.md) | `POST /users/phpass` | [docs](https://appwrite.io/docs/references/cloud/server-rest/users) |
| [Create user with Scrypt modified password](actions/users-create-scrypt-modified-user.md) | `POST /users/scrypt-modified` | [docs](https://appwrite.io/docs/references/cloud/server-rest/users) |
| [Create user with Scrypt password](actions/users-create-scrypt-user.md) | `POST /users/scrypt` | [docs](https://appwrite.io/docs/references/cloud/server-rest/users) |
| [Create session](actions/users-create-session.md) | `POST /users/{userId}/sessions` | [docs](https://appwrite.io/docs/references/cloud/server-rest/users) |
| [Create user with SHA password](actions/users-create-shauser.md) | `POST /users/sha` | [docs](https://appwrite.io/docs/references/cloud/server-rest/users) |
| [Create user target](actions/users-create-target.md) | `POST /users/{userId}/targets` | [docs](https://appwrite.io/docs/references/cloud/server-rest/users) |
| [Create token](actions/users-create-token.md) | `POST /users/{userId}/tokens` | [docs](https://appwrite.io/docs/references/cloud/server-rest/users) |
| [Delete user](actions/users-delete.md) | `DELETE /users/{userId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/users) |
| [Delete identity](actions/users-delete-identity.md) | `DELETE /users/identities/{identityId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/users) |
| [Delete authenticator](actions/users-delete-mfa-authenticator.md) | `DELETE /users/{userId}/mfa/authenticators/{type}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/users) |
| [Delete user session](actions/users-delete-session.md) | `DELETE /users/{userId}/sessions/{sessionId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/users) |
| [Delete user sessions](actions/users-delete-sessions.md) | `DELETE /users/{userId}/sessions` | [docs](https://appwrite.io/docs/references/cloud/server-rest/users) |
| [Delete user target](actions/users-delete-target.md) | `DELETE /users/{userId}/targets/{targetId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/users) |
| [Get user](actions/users-get.md) | `GET /users/{userId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/users) |
| [Get MFA recovery codes](actions/users-get-mfa-recovery-codes.md) | `GET /users/{userId}/mfa/recovery-codes` | [docs](https://appwrite.io/docs/references/cloud/server-rest/users) |
| [Get user preferences](actions/users-get-prefs.md) | `GET /users/{userId}/prefs` | [docs](https://appwrite.io/docs/references/cloud/server-rest/users) |
| [Get user target](actions/users-get-target.md) | `GET /users/{userId}/targets/{targetId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/users) |
| [List users](actions/users-list.md) | `GET /users` | [docs](https://appwrite.io/docs/references/cloud/server-rest/users) |
| [List identities](actions/users-list-identities.md) | `GET /users/identities` | [docs](https://appwrite.io/docs/references/cloud/server-rest/users) |
| [List user logs](actions/users-list-logs.md) | `GET /users/{userId}/logs` | [docs](https://appwrite.io/docs/references/cloud/server-rest/users) |
| [List user memberships](actions/users-list-memberships.md) | `GET /users/{userId}/memberships` | [docs](https://appwrite.io/docs/references/cloud/server-rest/users) |
| [List factors](actions/users-list-mfa-factors.md) | `GET /users/{userId}/mfa/factors` | [docs](https://appwrite.io/docs/references/cloud/server-rest/users) |
| [List user sessions](actions/users-list-sessions.md) | `GET /users/{userId}/sessions` | [docs](https://appwrite.io/docs/references/cloud/server-rest/users) |
| [List user targets](actions/users-list-targets.md) | `GET /users/{userId}/targets` | [docs](https://appwrite.io/docs/references/cloud/server-rest/users) |
| [Update email](actions/users-update-email.md) | `PATCH /users/{userId}/email` | [docs](https://appwrite.io/docs/references/cloud/server-rest/users) |
| [Update email verification](actions/users-update-email-verification.md) | `PATCH /users/{userId}/verification` | [docs](https://appwrite.io/docs/references/cloud/server-rest/users) |
| [Update user labels](actions/users-update-labels.md) | `PUT /users/{userId}/labels` | [docs](https://appwrite.io/docs/references/cloud/server-rest/users) |
| [Update MFA](actions/users-update-mfa.md) | `PATCH /users/{userId}/mfa` | [docs](https://appwrite.io/docs/references/cloud/server-rest/users) |
| [Update MFA recovery codes (regenerate)](actions/users-update-mfa-recovery-codes.md) | `PUT /users/{userId}/mfa/recovery-codes` | [docs](https://appwrite.io/docs/references/cloud/server-rest/users) |
| [Update name](actions/users-update-name.md) | `PATCH /users/{userId}/name` | [docs](https://appwrite.io/docs/references/cloud/server-rest/users) |
| [Update password](actions/users-update-password.md) | `PATCH /users/{userId}/password` | [docs](https://appwrite.io/docs/references/cloud/server-rest/users) |
| [Update phone](actions/users-update-phone.md) | `PATCH /users/{userId}/phone` | [docs](https://appwrite.io/docs/references/cloud/server-rest/users) |
| [Update phone verification](actions/users-update-phone-verification.md) | `PATCH /users/{userId}/verification/phone` | [docs](https://appwrite.io/docs/references/cloud/server-rest/users) |
| [Update user preferences](actions/users-update-prefs.md) | `PATCH /users/{userId}/prefs` | [docs](https://appwrite.io/docs/references/cloud/server-rest/users) |
| [Update user status](actions/users-update-status.md) | `PATCH /users/{userId}/status` | [docs](https://appwrite.io/docs/references/cloud/server-rest/users) |
| [Update user target](actions/users-update-target.md) | `PATCH /users/{userId}/targets/{targetId}` | [docs](https://appwrite.io/docs/references/cloud/server-rest/users) |
