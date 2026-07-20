# <img src="https://images.mindcloud.co/apps/icons/appwrite-icon-square-512_1776361772256.png" alt="Appwrite logo" width="28" height="28"> Appwrite: Universal API

Appwrite official server API wrapper built from the Appwrite 1.8.x OpenAPI.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/appwrite/latest
- **Actions:** 375
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://appwrite.io
- **Vendor API docs:** https://appwrite.io/docs/apis/rest

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List users](actions/users-list.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/users-list?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (375)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Create file token](actions/tokens-create-file-token.md) | POST | Creates a new file token in your Appwrite project. |
| [Delete token](actions/tokens-delete.md) | DELETE | Deletes the token from your Appwrite project. |
| [Get token](actions/tokens-get.md) | GET | Retrieves token details from your Appwrite project. |
| [List tokens](actions/tokens-list.md) | GET | Retrieves a list of tokens from your Appwrite project. |
| [Update token](actions/tokens-update.md) | PUT | Updates the token in your Appwrite project. |

### Builds

| Action | Method | Description |
| --- | --- | --- |
| [Create function](actions/functions-create.md) | POST | Creates a new function in your Appwrite project. |
| [Create deployment](actions/functions-create-deployment.md) | POST | Creates a new deployment in your Appwrite project. |
| [Create duplicate deployment](actions/functions-create-duplicate-deployment.md) | POST | Creates a new duplicate deployment in your Appwrite project. |
| [Create execution](actions/functions-create-execution.md) | POST | Creates a new execution in your Appwrite project. |
| [Create template deployment](actions/functions-create-template-deployment.md) | POST | Creates a new template deployment in your Appwrite project. |
| [Create variable](actions/functions-create-variable.md) | POST | Creates a new variable in your Appwrite project. |
| [Create VCS deployment](actions/functions-create-vcs-deployment.md) | POST | Creates a new VCS deployment in your Appwrite project. |
| [Delete function](actions/functions-delete.md) | DELETE | Deletes the function from your Appwrite project. |
| [Delete deployment](actions/functions-delete-deployment.md) | DELETE | Deletes the deployment from your Appwrite project. |
| [Delete execution](actions/functions-delete-execution.md) | DELETE | Deletes the execution from your Appwrite project. |
| [Delete variable](actions/functions-delete-variable.md) | DELETE | Deletes the variable from your Appwrite project. |
| [Get function](actions/functions-get.md) | GET | Retrieves function details from your Appwrite project. |
| [Get deployment](actions/functions-get-deployment.md) | GET | Retrieves the deployment from your Appwrite project. |
| [Get deployment download](actions/functions-get-deployment-download.md) | GET | Retrieves the deployment download from your Appwrite project. |
| [Get execution](actions/functions-get-execution.md) | GET | Retrieves the execution from your Appwrite project. |
| [Get variable](actions/functions-get-variable.md) | GET | Retrieves the variable from your Appwrite project. |
| [List functions](actions/functions-list.md) | GET | Retrieves a list of functions from your Appwrite project. |
| [List deployments](actions/functions-list-deployments.md) | GET | Retrieves a list of deployments from your Appwrite project. |
| [List executions](actions/functions-list-executions.md) | GET | Retrieves a list of executions from your Appwrite project. |
| [List runtimes](actions/functions-list-runtimes.md) | GET | Retrieves a list of runtimes from your Appwrite project. |
| [List specifications](actions/functions-list-specifications.md) | GET | Retrieves a list of specifications from your Appwrite project. |
| [List variables](actions/functions-list-variables.md) | GET | Retrieves a list of variables from your Appwrite project. |
| [Update function](actions/functions-update.md) | PUT | Updates the function in your Appwrite project. |
| [Update deployment status](actions/functions-update-deployment-status.md) | PUT | Updates the deployment status in your Appwrite project. |
| [Update function's deployment](actions/functions-update-function-deployment.md) | PUT | Updates a function deployment in your Appwrite project. |
| [Update variable](actions/functions-update-variable.md) | PUT | Updates the variable in your Appwrite project. |
| [Get builds queue](actions/health-get-queue-builds.md) | GET | Retrieves Appwrite builds queue metrics. |
| [Create deployment](actions/sites-create-deployment.md) | POST | Creates a new deployment in your Appwrite project. |

### Databases

| Action | Method | Description |
| --- | --- | --- |
| [Create database](actions/databases-create.md) | POST | Creates a new database in your Appwrite project. |
| [Create boolean attribute](actions/databases-create-boolean-attribute.md) | POST | Creates a new boolean attribute in your Appwrite project. |
| [Create collections](actions/databases-create-collection.md) | POST | Creates collections in your Appwrite project. |
| [Create datetime attribute](actions/databases-create-datetime-attribute.md) | POST | Creates a new datetime attribute in your Appwrite project. |
| [Create document](actions/databases-create-document.md) | POST | Creates a new document in your Appwrite project. |
| [Create email attribute](actions/databases-create-email-attribute.md) | POST | Creates a new email attribute in your Appwrite project. |
| [Create enum attribute](actions/databases-create-enum-attribute.md) | POST | Creates a new enum attribute in your Appwrite project. |
| [Create float attribute](actions/databases-create-float-attribute.md) | POST | Creates a new float attribute in your Appwrite project. |
| [Create index](actions/databases-create-index.md) | POST | Creates a new index in your Appwrite project. |
| [Create integer attribute](actions/databases-create-integer-attribute.md) | POST | Creates a new integer attribute in your Appwrite project. |
| [Create IP address attribute](actions/databases-create-ip-attribute.md) | POST | Creates a new IP address attribute in your Appwrite project. |
| [Create line attribute](actions/databases-create-line-attribute.md) | POST | Creates a new line attribute in your Appwrite project. |
| [Create operations](actions/databases-create-operations.md) | POST | Creates operations in your Appwrite project. |
| [Create point attribute](actions/databases-create-point-attribute.md) | POST | Creates a new point attribute in your Appwrite project. |
| [Create polygon attribute](actions/databases-create-polygon-attribute.md) | POST | Creates a new polygon attribute in your Appwrite project. |
| [Create relationship attribute](actions/databases-create-relationship-attribute.md) | POST | Creates a new relationship attribute in your Appwrite project. |
| [Create string attribute](actions/databases-create-string-attribute.md) | POST | Creates a new string attribute in your Appwrite project. |
| [Create transaction](actions/databases-create-transaction.md) | POST | Creates a new transaction in your Appwrite project. |
| [Create URL attribute](actions/databases-create-url-attribute.md) | POST | Creates a new URL attribute in your Appwrite project. |
| [Decrement document attribute](actions/databases-decrement-document-attribute.md) | PUT | Decrements the document attribute in your Appwrite project. |
| [Delete database](actions/databases-delete.md) | DELETE | Deletes the database from your Appwrite project. |
| [Delete attribute](actions/databases-delete-attribute.md) | DELETE | Deletes the attribute from your Appwrite project. |
| [Delete collection](actions/databases-delete-collection.md) | DELETE | Deletes the collection from your Appwrite project. |
| [Delete document](actions/databases-delete-document.md) | DELETE | Deletes the document from your Appwrite project. |
| [Delete documents](actions/databases-delete-documents.md) | DELETE | Deletes documents from your Appwrite project. |
| [Delete index](actions/databases-delete-index.md) | DELETE | Deletes the index from your Appwrite project. |
| [Delete transaction](actions/databases-delete-transaction.md) | DELETE | Deletes the transaction from your Appwrite project. |
| [Get database](actions/databases-get.md) | GET | Retrieves database details from your Appwrite project. |
| [Get attribute](actions/databases-get-attribute.md) | GET | Retrieves the attribute from your Appwrite project. |
| [Get collection](actions/databases-get-collection.md) | GET | Retrieves collection details from your Appwrite project. |
| [Get document](actions/databases-get-document.md) | GET | Retrieves the document from your Appwrite project. |
| [Get index](actions/databases-get-index.md) | GET | Retrieves the index from your Appwrite project. |
| [Get transaction](actions/databases-get-transaction.md) | GET | Retrieves transaction details from your Appwrite project. |
| [Increment document attribute](actions/databases-increment-document-attribute.md) | PUT | Increments the document attribute in your Appwrite project. |
| [List databases](actions/databases-list.md) | GET | Retrieves a list of databases from your Appwrite project. |
| [List attributes](actions/databases-list-attributes.md) | GET | Retrieves a list of attributes from your Appwrite project. |
| [List collections](actions/databases-list-collections.md) | GET | Retrieves a list of collections from your Appwrite project. |
| [List documents](actions/databases-list-documents.md) | GET | Retrieves a list of documents from your Appwrite project. |
| [List indexes](actions/databases-list-indexes.md) | GET | Retrieves a list of indexes from your Appwrite project. |
| [List transactions](actions/databases-list-transactions.md) | GET | Retrieves a list of transactions from your Appwrite project. |
| [Update database](actions/databases-update.md) | PUT | Updates the database in your Appwrite project. |
| [Update boolean attribute](actions/databases-update-boolean-attribute.md) | PUT | Updates the boolean attribute in your Appwrite project. |
| [Update collection](actions/databases-update-collection.md) | PUT | Updates the collection in your Appwrite project. |
| [Update datetime attribute](actions/databases-update-datetime-attribute.md) | PUT | Updates the datetime attribute in your Appwrite project. |
| [Update document](actions/databases-update-document.md) | PUT | Updates the document in your Appwrite project. |
| [Update documents](actions/databases-update-documents.md) | PUT | Updates the documents in your Appwrite project. |
| [Update email attribute](actions/databases-update-email-attribute.md) | PUT | Updates the email attribute in your Appwrite project. |
| [Update enum attribute](actions/databases-update-enum-attribute.md) | PUT | Updates the enum attribute in your Appwrite project. |
| [Update float attribute](actions/databases-update-float-attribute.md) | PUT | Updates the float attribute in your Appwrite project. |
| [Update integer attribute](actions/databases-update-integer-attribute.md) | PUT | Updates the integer attribute in your Appwrite project. |
| [Update IP address attribute](actions/databases-update-ip-attribute.md) | PUT | Updates the IP address attribute in your Appwrite project. |
| [Update line attribute](actions/databases-update-line-attribute.md) | PUT | Updates the line attribute in your Appwrite project. |
| [Update point attribute](actions/databases-update-point-attribute.md) | PUT | Updates the point attribute in your Appwrite project. |
| [Update polygon attribute](actions/databases-update-polygon-attribute.md) | PUT | Updates the polygon attribute in your Appwrite project. |
| [Update relationship attribute](actions/databases-update-relationship-attribute.md) | PUT | Updates the relationship attribute in your Appwrite project. |
| [Update string attribute](actions/databases-update-string-attribute.md) | PUT | Updates the string attribute in your Appwrite project. |
| [Update transaction](actions/databases-update-transaction.md) | PUT | Updates the transaction in your Appwrite project. |
| [Update URL attribute](actions/databases-update-url-attribute.md) | PUT | Updates the URL attribute in your Appwrite project. |
| [Upsert a document](actions/databases-upsert-document.md) | PUT | Upserts a document in your Appwrite project. |
| [Upsert documents](actions/databases-upsert-documents.md) | PUT | Upserts documents in your Appwrite project. |
| [Create database](actions/tables-dbcreate.md) | POST | Creates a new database in your Appwrite project. |
| [Create boolean column](actions/tables-dbcreate-boolean-column.md) | POST | Creates a new boolean column in your Appwrite project. |
| [Create datetime column](actions/tables-dbcreate-datetime-column.md) | POST | Creates a new datetime column in your Appwrite project. |
| [Create email column](actions/tables-dbcreate-email-column.md) | POST | Creates a new email column in your Appwrite project. |
| [Create enum column](actions/tables-dbcreate-enum-column.md) | POST | Creates a new enum column in your Appwrite project. |
| [Create float column](actions/tables-dbcreate-float-column.md) | POST | Creates a new float column in your Appwrite project. |
| [Create index](actions/tables-dbcreate-index.md) | POST | Creates a new index in your Appwrite project. |
| [Create integer column](actions/tables-dbcreate-integer-column.md) | POST | Creates a new integer column in your Appwrite project. |
| [Create IP address column](actions/tables-dbcreate-ip-column.md) | POST | Creates a new IP address column in your Appwrite project. |
| [Create line column](actions/tables-dbcreate-line-column.md) | POST | Creates a new line column in your Appwrite project. |
| [Create operations](actions/tables-dbcreate-operations.md) | POST | Creates operations in your Appwrite project. |
| [Create point column](actions/tables-dbcreate-point-column.md) | POST | Creates a new point column in your Appwrite project. |
| [Create polygon column](actions/tables-dbcreate-polygon-column.md) | POST | Creates a new polygon column in your Appwrite project. |
| [Create relationship column](actions/tables-dbcreate-relationship-column.md) | POST | Creates a new relationship column in your Appwrite project. |
| [Create row](actions/tables-dbcreate-row.md) | POST | Creates a new row in your Appwrite project. |
| [Create string column](actions/tables-dbcreate-string-column.md) | POST | Creates a new string column in your Appwrite project. |
| [Create table](actions/tables-dbcreate-table.md) | POST | Creates a new table in your Appwrite project. |
| [Create transaction](actions/tables-dbcreate-transaction.md) | POST | Creates a new transaction in your Appwrite project. |
| [Create URL column](actions/tables-dbcreate-url-column.md) | POST | Creates a new URL column in your Appwrite project. |
| [Decrement row column](actions/tables-dbdecrement-row-column.md) | PUT | Decrements the row column in your Appwrite project. |
| [Delete database](actions/tables-dbdelete.md) | DELETE | Deletes the database from your Appwrite project. |
| [Delete column](actions/tables-dbdelete-column.md) | DELETE | Deletes the column from your Appwrite project. |
| [Delete index](actions/tables-dbdelete-index.md) | DELETE | Deletes the index from your Appwrite project. |
| [Delete row](actions/tables-dbdelete-row.md) | DELETE | Deletes the row from your Appwrite project. |
| [Delete rows](actions/tables-dbdelete-rows.md) | DELETE | Deletes rows from your Appwrite project. |
| [Delete table](actions/tables-dbdelete-table.md) | DELETE | Deletes the table from your Appwrite project. |
| [Delete transaction](actions/tables-dbdelete-transaction.md) | DELETE | Deletes the transaction from your Appwrite project. |
| [Get database](actions/tables-dbget.md) | GET | Retrieves database details from your Appwrite project. |
| [Get column](actions/tables-dbget-column.md) | GET | Retrieves the column from your Appwrite project. |
| [Get index](actions/tables-dbget-index.md) | GET | Retrieves the index from your Appwrite project. |
| [Get row](actions/tables-dbget-row.md) | GET | Retrieves the row from your Appwrite project. |
| [Get table](actions/tables-dbget-table.md) | GET | Retrieves the table from your Appwrite project. |
| [Get transaction](actions/tables-dbget-transaction.md) | GET | Retrieves transaction details from your Appwrite project. |
| [Increment row column](actions/tables-dbincrement-row-column.md) | PUT | Increments the row column in your Appwrite project. |
| [List databases](actions/tables-dblist.md) | GET | Retrieves a list of databases from your Appwrite project. |
| [List columns](actions/tables-dblist-columns.md) | GET | Retrieves a list of columns from your Appwrite project. |
| [List indexes](actions/tables-dblist-indexes.md) | GET | Retrieves a list of indexes from your Appwrite project. |
| [List rows](actions/tables-dblist-rows.md) | GET | Retrieves a list of rows from your Appwrite project. |
| [List tables](actions/tables-dblist-tables.md) | GET | Retrieves a list of tables from your Appwrite project. |
| [List transactions](actions/tables-dblist-transactions.md) | GET | Retrieves a list of transactions from your Appwrite project. |
| [Update database](actions/tables-dbupdate.md) | PUT | Updates the database in your Appwrite project. |
| [Update boolean column](actions/tables-dbupdate-boolean-column.md) | PUT | Updates the boolean column in your Appwrite project. |
| [Update dateTime column](actions/tables-dbupdate-datetime-column.md) | PUT | Updates the dateTime column in your Appwrite project. |
| [Update email column](actions/tables-dbupdate-email-column.md) | PUT | Updates the email column in your Appwrite project. |
| [Update enum column](actions/tables-dbupdate-enum-column.md) | PUT | Updates the enum column in your Appwrite project. |
| [Update float column](actions/tables-dbupdate-float-column.md) | PUT | Updates the float column in your Appwrite project. |
| [Update integer column](actions/tables-dbupdate-integer-column.md) | PUT | Updates the integer column in your Appwrite project. |
| [Update IP address column](actions/tables-dbupdate-ip-column.md) | PUT | Updates the IP address column in your Appwrite project. |
| [Update line column](actions/tables-dbupdate-line-column.md) | PUT | Updates the line column in your Appwrite project. |
| [Update point column](actions/tables-dbupdate-point-column.md) | PUT | Updates the point column in your Appwrite project. |
| [Update polygon column](actions/tables-dbupdate-polygon-column.md) | PUT | Updates the polygon column in your Appwrite project. |
| [Update relationship column](actions/tables-dbupdate-relationship-column.md) | PUT | Updates the relationship column in your Appwrite project. |
| [Update row](actions/tables-dbupdate-row.md) | PUT | Updates the row in your Appwrite project. |
| [Update rows](actions/tables-dbupdate-rows.md) | PUT | Updates the rows in your Appwrite project. |
| [Update string column](actions/tables-dbupdate-string-column.md) | PUT | Updates the string column in your Appwrite project. |
| [Update table](actions/tables-dbupdate-table.md) | PUT | Updates the table in your Appwrite project. |
| [Update transaction](actions/tables-dbupdate-transaction.md) | PUT | Updates the transaction in your Appwrite project. |
| [Update URL column](actions/tables-dbupdate-url-column.md) | PUT | Updates the URL column in your Appwrite project. |
| [Upsert a row](actions/tables-dbupsert-row.md) | PUT | Upserts a row in your Appwrite project. |
| [Upsert rows](actions/tables-dbupsert-rows.md) | PUT | Upserts rows in your Appwrite project. |

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [Create email password session](actions/account-create-email-password-session.md) | POST | Creates a new email password session in your Appwrite project. |
| [Create email token (OTP)](actions/account-create-email-token.md) | POST | Creates a new email token OTP in your Appwrite project. |
| [Create email verification](actions/account-create-email-verification.md) | POST | Creates a new email verification in your Appwrite project. |
| [Update email](actions/account-update-email.md) | PUT | Updates the email in your Appwrite project. |
| [Update email verification (confirmation)](actions/account-update-email-verification.md) | PUT | Completes email verification flow in Appwrite. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Create bucket](actions/storage-create-bucket.md) | POST | Creates a new bucket in your Appwrite project. |
| [Create file](actions/storage-create-file.md) | POST | Creates a new file in your Appwrite project. |
| [Delete bucket](actions/storage-delete-bucket.md) | DELETE | Deletes the bucket from your Appwrite project. |
| [Delete file](actions/storage-delete-file.md) | DELETE | Deletes the file from your Appwrite project. |
| [Get bucket](actions/storage-get-bucket.md) | GET | Retrieves bucket details from your Appwrite project. |
| [Get file](actions/storage-get-file.md) | GET | Retrieves file details from Appwrite storage. |
| [Get file for download](actions/storage-get-file-download.md) | GET | Downloads a file from Appwrite storage. |
| [Get file preview](actions/storage-get-file-preview.md) | GET | Retrieves the file preview from your Appwrite project. |
| [Get file for view](actions/storage-get-file-view.md) | GET | Views a file from Appwrite storage. |
| [List buckets](actions/storage-list-buckets.md) | GET | Retrieves a list of buckets from your Appwrite project. |
| [List files](actions/storage-list-files.md) | GET | Retrieves a list of files from your Appwrite project. |
| [Update bucket](actions/storage-update-bucket.md) | PUT | Updates the bucket in your Appwrite project. |
| [Update file](actions/storage-update-file.md) | PUT | Updates the file in your Appwrite project. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Create APNS provider](actions/messaging-create-apns-provider.md) | POST | Creates a new APNS provider in your Appwrite project. |
| [Create email](actions/messaging-create-email.md) | POST | Creates a new email in your Appwrite project. |
| [Create FCM provider](actions/messaging-create-fcm-provider.md) | POST | Creates a new FCM provider in your Appwrite project. |
| [Create Mailgun provider](actions/messaging-create-mailgun-provider.md) | POST | Creates a new mailgun provider in your Appwrite project. |
| [Create Msg91 provider](actions/messaging-create-msg91-provider.md) | POST | Creates a new Msg91 provider in your Appwrite project. |
| [Create push notification](actions/messaging-create-push.md) | POST | Creates a new push notification in your Appwrite project. |
| [Create Resend provider](actions/messaging-create-resend-provider.md) | POST | Creates a new resend provider in your Appwrite project. |
| [Create Sendgrid provider](actions/messaging-create-sendgrid-provider.md) | POST | Creates a new sendgrid provider in your Appwrite project. |
| [Create SMS](actions/messaging-create-sms.md) | POST | Creates SMS in your Appwrite project. |
| [Create SMTP provider](actions/messaging-create-smtp-provider.md) | POST | Creates a new SMTP provider in your Appwrite project. |
| [Create subscriber](actions/messaging-create-subscriber.md) | POST | Creates a new subscriber in your Appwrite project. |
| [Create Telesign provider](actions/messaging-create-telesign-provider.md) | POST | Creates a new telesign provider in your Appwrite project. |
| [Create Textmagic provider](actions/messaging-create-textmagic-provider.md) | POST | Creates a new textmagic provider in your Appwrite project. |
| [Create topic](actions/messaging-create-topic.md) | POST | Creates a new topic in your Appwrite project. |
| [Create Twilio provider](actions/messaging-create-twilio-provider.md) | POST | Creates a new twilio provider in your Appwrite project. |
| [Create Vonage provider](actions/messaging-create-vonage-provider.md) | POST | Creates a new vonage provider in your Appwrite project. |
| [Delete message](actions/messaging-delete.md) | DELETE | Deletes the message from your Appwrite project. |
| [Delete provider](actions/messaging-delete-provider.md) | DELETE | Deletes the provider from your Appwrite project. |
| [Delete subscriber](actions/messaging-delete-subscriber.md) | DELETE | Deletes the subscriber from your Appwrite project. |
| [Delete topic](actions/messaging-delete-topic.md) | DELETE | Deletes the topic from your Appwrite project. |
| [Get message](actions/messaging-get-message.md) | GET | Retrieves the message from your Appwrite project. |
| [Get provider](actions/messaging-get-provider.md) | GET | Retrieves the provider from your Appwrite project. |
| [Get subscriber](actions/messaging-get-subscriber.md) | GET | Retrieves the subscriber from your Appwrite project. |
| [Get topic](actions/messaging-get-topic.md) | GET | Retrieves the topic from your Appwrite project. |
| [List message logs](actions/messaging-list-message-logs.md) | GET | Retrieves a list of message logs from your Appwrite project. |
| [List messages](actions/messaging-list-messages.md) | GET | Retrieves a list of messages from your Appwrite project. |
| [List provider logs](actions/messaging-list-provider-logs.md) | GET | Retrieves a list of provider logs from your Appwrite project. |
| [List providers](actions/messaging-list-providers.md) | GET | Retrieves a list of providers from your Appwrite project. |
| [List subscriber logs](actions/messaging-list-subscriber-logs.md) | GET | Retrieves a list of subscriber logs from your Appwrite project. |
| [List subscribers](actions/messaging-list-subscribers.md) | GET | Retrieves a list of subscribers from your Appwrite project. |
| [List message targets](actions/messaging-list-targets.md) | GET | Retrieves a list of message targets from your Appwrite project. |
| [List topic logs](actions/messaging-list-topic-logs.md) | GET | Retrieves a list of topic logs from your Appwrite project. |
| [List topics](actions/messaging-list-topics.md) | GET | Retrieves a list of topics from your Appwrite project. |
| [Update APNS provider](actions/messaging-update-apns-provider.md) | PUT | Updates the APNS provider in your Appwrite project. |
| [Update email](actions/messaging-update-email.md) | PUT | Updates the email in your Appwrite project. |
| [Update FCM provider](actions/messaging-update-fcm-provider.md) | PUT | Updates the FCM provider in your Appwrite project. |
| [Update Mailgun provider](actions/messaging-update-mailgun-provider.md) | PUT | Updates the mailgun provider in your Appwrite project. |
| [Update Msg91 provider](actions/messaging-update-msg91-provider.md) | PUT | Updates the Msg91 provider in your Appwrite project. |
| [Update push notification](actions/messaging-update-push.md) | PUT | Updates the push notification in your Appwrite project. |
| [Update Resend provider](actions/messaging-update-resend-provider.md) | PUT | Updates the resend provider in your Appwrite project. |
| [Update Sendgrid provider](actions/messaging-update-sendgrid-provider.md) | PUT | Updates the sendgrid provider in your Appwrite project. |
| [Update SMS](actions/messaging-update-sms.md) | PUT | Updates the SMS in your Appwrite project. |
| [Update SMTP provider](actions/messaging-update-smtp-provider.md) | PUT | Updates the SMTP provider in your Appwrite project. |
| [Update Telesign provider](actions/messaging-update-telesign-provider.md) | PUT | Updates the telesign provider in your Appwrite project. |
| [Update Textmagic provider](actions/messaging-update-textmagic-provider.md) | PUT | Updates the textmagic provider in your Appwrite project. |
| [Update topic](actions/messaging-update-topic.md) | PUT | Updates the topic in your Appwrite project. |
| [Update Twilio provider](actions/messaging-update-twilio-provider.md) | PUT | Updates the twilio provider in your Appwrite project. |
| [Update Vonage provider](actions/messaging-update-vonage-provider.md) | PUT | Updates the vonage provider in your Appwrite project. |

### Pages

| Action | Method | Description |
| --- | --- | --- |
| [Create site](actions/sites-create.md) | POST | Creates a new site in your Appwrite project. |
| [Create duplicate deployment](actions/sites-create-duplicate-deployment.md) | POST | Creates a new duplicate deployment in your Appwrite project. |
| [Create template deployment](actions/sites-create-template-deployment.md) | POST | Creates a new template deployment in your Appwrite project. |
| [Create variable](actions/sites-create-variable.md) | POST | Creates a new variable in your Appwrite project. |
| [Create VCS deployment](actions/sites-create-vcs-deployment.md) | POST | Creates a new VCS deployment in your Appwrite project. |
| [Delete site](actions/sites-delete.md) | DELETE | Deletes the site from your Appwrite project. |
| [Delete deployment](actions/sites-delete-deployment.md) | DELETE | Deletes the deployment from your Appwrite project. |
| [Delete log](actions/sites-delete-log.md) | DELETE | Deletes the log from your Appwrite project. |
| [Delete variable](actions/sites-delete-variable.md) | DELETE | Deletes the variable from your Appwrite project. |
| [Get site](actions/sites-get.md) | GET | Retrieves site details from your Appwrite project. |
| [Get deployment](actions/sites-get-deployment.md) | GET | Retrieves the deployment from your Appwrite project. |
| [Get deployment download](actions/sites-get-deployment-download.md) | GET | Retrieves the deployment download from your Appwrite project. |
| [Get log](actions/sites-get-log.md) | GET | Retrieves the log from your Appwrite project. |
| [Get variable](actions/sites-get-variable.md) | GET | Retrieves the variable from your Appwrite project. |
| [List sites](actions/sites-list.md) | GET | Retrieves a list of sites from your Appwrite project. |
| [List deployments](actions/sites-list-deployments.md) | GET | Retrieves a list of deployments from your Appwrite project. |
| [List frameworks](actions/sites-list-frameworks.md) | GET | Retrieves a list of frameworks from your Appwrite project. |
| [List logs](actions/sites-list-logs.md) | GET | Retrieves a list of logs from your Appwrite project. |
| [List specifications](actions/sites-list-specifications.md) | GET | Retrieves a list of specifications from your Appwrite project. |
| [List variables](actions/sites-list-variables.md) | GET | Retrieves a list of variables from your Appwrite project. |
| [Update site](actions/sites-update.md) | PUT | Updates the site in your Appwrite project. |
| [Update deployment status](actions/sites-update-deployment-status.md) | PUT | Updates the deployment status in your Appwrite project. |
| [Update site's deployment](actions/sites-update-site-deployment.md) | PUT | Updates a site deployment in your Appwrite project. |
| [Update variable](actions/sites-update-variable.md) | PUT | Updates the variable in your Appwrite project. |

### Queues

| Action | Method | Description |
| --- | --- | --- |
| [Get logs queue](actions/health-get-queue-logs.md) | GET | Retrieves Appwrite logs queue metrics. |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Delete session](actions/account-delete-session.md) | DELETE | Deletes the session from your Appwrite project. |
| [Delete sessions](actions/account-delete-sessions.md) | DELETE | Deletes sessions from your Appwrite project. |
| [Get session](actions/account-get-session.md) | GET | Retrieves session details from Appwrite. |
| [List sessions](actions/account-list-sessions.md) | GET | Retrieves a list of sessions from your Appwrite project. |
| [Update session](actions/account-update-session.md) | PUT | Updates the session in your Appwrite project. |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [Create team](actions/teams-create.md) | POST | Creates a new team in your Appwrite project. |
| [Create team membership](actions/teams-create-membership.md) | POST | Creates a new team membership in your Appwrite project. |
| [Delete team](actions/teams-delete.md) | DELETE | Deletes the team from your Appwrite project. |
| [Delete team membership](actions/teams-delete-membership.md) | DELETE | Deletes the team membership from your Appwrite project. |
| [Get team](actions/teams-get.md) | GET | Retrieves team details from your Appwrite project. |
| [Get team membership](actions/teams-get-membership.md) | GET | Retrieves the team membership from your Appwrite project. |
| [Get team preferences](actions/teams-get-prefs.md) | GET | Retrieves the team preferences from your Appwrite project. |
| [List teams](actions/teams-list.md) | GET | Retrieves a list of teams from your Appwrite project. |
| [List team memberships](actions/teams-list-memberships.md) | GET | Retrieves a list of team memberships from your Appwrite project. |
| [Update membership](actions/teams-update-membership.md) | PUT | Updates the membership in your Appwrite project. |
| [Update team membership status](actions/teams-update-membership-status.md) | PUT | Updates the team membership status in your Appwrite project. |
| [Update name](actions/teams-update-name.md) | PUT | Updates the name in your Appwrite project. |
| [Update preferences](actions/teams-update-prefs.md) | PUT | Updates the preferences in your Appwrite project. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Create account](actions/account-create.md) | POST | Creates a new account in your Appwrite project. |
| [Create anonymous session](actions/account-create-anonymous-session.md) | POST | Creates a new anonymous session in your Appwrite project. |
| [Create JWT](actions/account-create-jwt.md) | POST | Creates a new JWT in your Appwrite project. |
| [Create magic URL token](actions/account-create-magic-urltoken.md) | POST | Creates a new magic URL token in your Appwrite project. |
| [Create authenticator](actions/account-create-mfa-authenticator.md) | POST | Creates a new authenticator in your Appwrite project. |
| [Create MFA challenge](actions/account-create-mfa-challenge.md) | POST | Creates a new MFA challenge in your Appwrite project. |
| [Create MFA recovery codes](actions/account-create-mfa-recovery-codes.md) | POST | Creates MFA recovery codes in your Appwrite project. |
| [Create OAuth2 token](actions/account-create-oauth2-token.md) | GET | Creates a new OAuth2 token in your Appwrite project. |
| [Create phone token](actions/account-create-phone-token.md) | POST | Creates a new phone token in your Appwrite project. |
| [Create phone verification](actions/account-create-phone-verification.md) | POST | Creates a new phone verification in your Appwrite project. |
| [Create password recovery](actions/account-create-recovery.md) | POST | Creates a new password recovery in your Appwrite project. |
| [Create session](actions/account-create-session.md) | POST | Creates a new session in your Appwrite project. |
| [Delete identity](actions/account-delete-identity.md) | DELETE | Deletes the identity from your Appwrite project. |
| [Delete authenticator](actions/account-delete-mfa-authenticator.md) | DELETE | Deletes the authenticator from your Appwrite project. |
| [Get account](actions/account-get.md) | GET | Retrieves account details from Appwrite. |
| [List MFA recovery codes](actions/account-get-mfa-recovery-codes.md) | GET | Retrieves a list of MFA recovery codes from your Appwrite project. |
| [Get account preferences](actions/account-get-prefs.md) | GET | Retrieves the account preferences from your Appwrite project. |
| [List identities](actions/account-list-identities.md) | GET | Retrieves a list of identities from your Appwrite project. |
| [List logs](actions/account-list-logs.md) | GET | Retrieves a list of logs from your Appwrite project. |
| [List factors](actions/account-list-mfa-factors.md) | GET | Retrieves a list of factors from your Appwrite project. |
| [Update magic URL session](actions/account-update-magic-urlsession.md) | PUT | Updates the magic URL session in your Appwrite project. |
| [Update MFA](actions/account-update-mfa.md) | PUT | Updates the MFA in your Appwrite project. |
| [Update authenticator (confirmation)](actions/account-update-mfa-authenticator.md) | PUT | Completes MFA authenticator setup in Appwrite. |
| [Update MFA challenge (confirmation)](actions/account-update-mfa-challenge.md) | PUT | Completes an MFA challenge in Appwrite. |
| [Update MFA recovery codes (regenerate)](actions/account-update-mfa-recovery-codes.md) | PUT | Regenerates MFA recovery codes in Appwrite. |
| [Update name](actions/account-update-name.md) | PUT | Updates the name in your Appwrite project. |
| [Update password](actions/account-update-password.md) | PUT | Updates the password in your Appwrite project. |
| [Update phone](actions/account-update-phone.md) | PUT | Updates the phone in your Appwrite project. |
| [Update phone session](actions/account-update-phone-session.md) | PUT | Updates the phone session in your Appwrite project. |
| [Update phone verification (confirmation)](actions/account-update-phone-verification.md) | PUT | Completes phone verification flow in Appwrite. |
| [Update preferences](actions/account-update-prefs.md) | PUT | Updates the preferences in your Appwrite project. |
| [Update password recovery (confirmation)](actions/account-update-recovery.md) | PUT | Completes password recovery flow in Appwrite. |
| [Update status](actions/account-update-status.md) | PUT | Updates the status in your Appwrite project. |
| [Get browser icon](actions/avatars-get-browser.md) | GET | Retrieves a browser icon from Appwrite. |
| [Get credit card icon](actions/avatars-get-credit-card.md) | GET | Retrieves a credit card icon from Appwrite. |
| [Get favicon](actions/avatars-get-favicon.md) | GET | Retrieves a favicon image from Appwrite. |
| [Get country flag](actions/avatars-get-flag.md) | GET | Retrieves a country flag from Appwrite. |
| [Get image from URL](actions/avatars-get-image.md) | GET | Retrieves an image from a URL with Appwrite. |
| [Get user initials](actions/avatars-get-initials.md) | GET | Retrieves a user initials avatar from Appwrite. |
| [Get QR code](actions/avatars-get-qr.md) | GET | Retrieves a QR code from Appwrite. |
| [Get webpage screenshot](actions/avatars-get-screenshot.md) | GET | Retrieves a webpage screenshot from Appwrite. |
| [GraphQL endpoint](actions/graphql-mutation.md) | POST | Makes a GraphQL mutation request to Appwrite. |
| [GraphQL endpoint](actions/graphql-query.md) | POST | Makes a GraphQL query request to Appwrite. |
| [Get HTTP](actions/health-get.md) | GET | Retrieves Appwrite HTTP health status. |
| [Get antivirus](actions/health-get-antivirus.md) | GET | Retrieves Appwrite antivirus health status. |
| [Get cache](actions/health-get-cache.md) | GET | Retrieves Appwrite cache health status. |
| [Get the SSL certificate for a domain](actions/health-get-certificate.md) | GET | Retrieves Appwrite SSL certificate details for a domain. |
| [Get DB](actions/health-get-db.md) | GET | Retrieves Appwrite database health status. |
| [Get number of failed queue jobs](actions/health-get-failed-jobs.md) | GET | Retrieves the number of failed Appwrite queue jobs. |
| [Get pubsub](actions/health-get-pub-sub.md) | GET | Retrieves Appwrite pubsub health status. |
| [Get certificates queue](actions/health-get-queue-certificates.md) | GET | Retrieves Appwrite certificates queue metrics. |
| [Get databases queue](actions/health-get-queue-databases.md) | GET | Retrieves Appwrite databases queue metrics. |
| [Get deletes queue](actions/health-get-queue-deletes.md) | GET | Retrieves Appwrite deletes queue metrics. |
| [Get functions queue](actions/health-get-queue-functions.md) | GET | Retrieves Appwrite functions queue metrics. |
| [Get mails queue](actions/health-get-queue-mails.md) | GET | Retrieves Appwrite mail queue metrics. |
| [Get messaging queue](actions/health-get-queue-messaging.md) | GET | Retrieves Appwrite messaging queue metrics. |
| [Get migrations queue](actions/health-get-queue-migrations.md) | GET | Retrieves Appwrite migrations queue metrics. |
| [Get stats resources queue](actions/health-get-queue-stats-resources.md) | GET | Retrieves Appwrite stats resources queue metrics. |
| [Get stats usage queue](actions/health-get-queue-usage.md) | GET | Retrieves Appwrite stats usage queue metrics. |
| [Get webhooks queue](actions/health-get-queue-webhooks.md) | GET | Retrieves Appwrite webhooks queue metrics. |
| [Get storage](actions/health-get-storage.md) | GET | Retrieves Appwrite storage health status. |
| [Get local storage](actions/health-get-storage-local.md) | GET | Retrieves Appwrite local storage health status. |
| [Get time](actions/health-get-time.md) | GET | Retrieves Appwrite server time details. |
| [Get user locale](actions/locale-get.md) | GET | Retrieves the user locale from Appwrite. |
| [List locale codes](actions/locale-list-codes.md) | GET | Retrieves a list of locale codes from Appwrite. |
| [List continents](actions/locale-list-continents.md) | GET | Retrieves a list of continents from Appwrite. |
| [List countries](actions/locale-list-countries.md) | GET | Retrieves a list of countries from Appwrite. |
| [List EU countries](actions/locale-list-countries-eu.md) | GET | Retrieves a list of EU countries from Appwrite. |
| [List countries phone codes](actions/locale-list-countries-phones.md) | GET | Retrieves a list of countries phone codes from Appwrite. |
| [List currencies](actions/locale-list-currencies.md) | GET | Retrieves a list of currencies from Appwrite. |
| [List languages](actions/locale-list-languages.md) | GET | Retrieves a list of languages from Appwrite. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create user](actions/users-create.md) | POST | Creates a new user in your Appwrite project. |
| [Create user with Argon2 password](actions/users-create-argon2-user.md) | POST | Creates a new user with Argon2 password in your Appwrite project. |
| [Create user with bcrypt password](actions/users-create-bcrypt-user.md) | POST | Creates a new user with bcrypt password in your Appwrite project. |
| [Create user JWT](actions/users-create-jwt.md) | POST | Creates a new user JWT in your Appwrite project. |
| [Create user with MD5 password](actions/users-create-md5-user.md) | POST | Creates a new user with MD5 password in your Appwrite project. |
| [Create MFA recovery codes](actions/users-create-mfa-recovery-codes.md) | PUT | Creates MFA recovery codes in your Appwrite project. |
| [Create user with PHPass password](actions/users-create-phpass-user.md) | POST | Creates a new user with PHPass password in your Appwrite project. |
| [Create user with Scrypt modified password](actions/users-create-scrypt-modified-user.md) | POST | Creates a new user with Scrypt modified password in your Appwrite project. |
| [Create user with Scrypt password](actions/users-create-scrypt-user.md) | POST | Creates a new user with Scrypt password in your Appwrite project. |
| [Create session](actions/users-create-session.md) | POST | Creates a new session in your Appwrite project. |
| [Create user with SHA password](actions/users-create-shauser.md) | POST | Creates a new user with SHA password in your Appwrite project. |
| [Create user target](actions/users-create-target.md) | POST | Creates a new user target in your Appwrite project. |
| [Create token](actions/users-create-token.md) | POST | Creates a new token in your Appwrite project. |
| [Delete user](actions/users-delete.md) | DELETE | Deletes the user from your Appwrite project. |
| [Delete identity](actions/users-delete-identity.md) | DELETE | Deletes the identity from your Appwrite project. |
| [Delete authenticator](actions/users-delete-mfa-authenticator.md) | DELETE | Deletes the authenticator from your Appwrite project. |
| [Delete user session](actions/users-delete-session.md) | DELETE | Deletes the user session from your Appwrite project. |
| [Delete user sessions](actions/users-delete-sessions.md) | DELETE | Deletes user sessions from your Appwrite project. |
| [Delete user target](actions/users-delete-target.md) | DELETE | Deletes the user target from your Appwrite project. |
| [Get user](actions/users-get.md) | GET | Retrieves user details from your Appwrite project. |
| [Get MFA recovery codes](actions/users-get-mfa-recovery-codes.md) | GET | Retrieves the MFA recovery codes from your Appwrite project. |
| [Get user preferences](actions/users-get-prefs.md) | GET | Retrieves the user preferences from your Appwrite project. |
| [Get user target](actions/users-get-target.md) | GET | Retrieves the user target from your Appwrite project. |
| [List users](actions/users-list.md) | GET | Retrieves a list of users from your Appwrite project. |
| [List identities](actions/users-list-identities.md) | GET | Retrieves a list of identities from your Appwrite project. |
| [List user logs](actions/users-list-logs.md) | GET | Retrieves a list of user logs from your Appwrite project. |
| [List user memberships](actions/users-list-memberships.md) | GET | Retrieves a list of user memberships from your Appwrite project. |
| [List factors](actions/users-list-mfa-factors.md) | GET | Retrieves a list of factors from your Appwrite project. |
| [List user sessions](actions/users-list-sessions.md) | GET | Retrieves a list of user sessions from your Appwrite project. |
| [List user targets](actions/users-list-targets.md) | GET | Retrieves a list of user targets from your Appwrite project. |
| [Update email](actions/users-update-email.md) | PUT | Updates the email in your Appwrite project. |
| [Update email verification](actions/users-update-email-verification.md) | PUT | Updates the email verification in your Appwrite project. |
| [Update user labels](actions/users-update-labels.md) | PUT | Updates the user labels in your Appwrite project. |
| [Update MFA](actions/users-update-mfa.md) | PUT | Updates the MFA in your Appwrite project. |
| [Update MFA recovery codes (regenerate)](actions/users-update-mfa-recovery-codes.md) | PUT | Regenerates MFA recovery codes in Appwrite. |
| [Update name](actions/users-update-name.md) | PUT | Updates the name in your Appwrite project. |
| [Update password](actions/users-update-password.md) | PUT | Updates the password in your Appwrite project. |
| [Update phone](actions/users-update-phone.md) | PUT | Updates the phone in your Appwrite project. |
| [Update phone verification](actions/users-update-phone-verification.md) | PUT | Updates the phone verification in your Appwrite project. |
| [Update user preferences](actions/users-update-prefs.md) | PUT | Updates the user preferences in your Appwrite project. |
| [Update user status](actions/users-update-status.md) | PUT | Updates the user status in your Appwrite project. |
| [Update user target](actions/users-update-target.md) | PUT | Updates the user target in your Appwrite project. |

