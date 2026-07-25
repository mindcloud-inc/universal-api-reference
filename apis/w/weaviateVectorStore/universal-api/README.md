# <img src="https://images.mindcloud.co/apps/icons/images-8_1775852878587.jpeg" alt="Weaviate Vector Store logo" width="28" height="28"> Weaviate Vector Store: Universal API

Manage Weaviate cluster health, collections, tenants, and vector objects through the cluster-specific REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/weaviateVectorStore/latest
- **Category:** IT Operations / Database
- **Actions:** 160
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://weaviate.io/
- **Vendor API docs:** https://docs.weaviate.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Cluster Meta](actions/get-cluster-meta.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/get-cluster-meta?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (160)

### Collections

| Action | Method | Description |
| --- | --- | --- |
| [Add a property to a collection](actions/add-a-property-to-a-collection.md) | POST | Adds a property to a collection in Weaviate. |
| [Add Collection Property](actions/add-collection-property.md) | PUT | Adds a property to a collection in Weaviate. |
| [Create Collection](actions/create-collection.md) | POST | Creates a new collection in Weaviate. |
| [Delete a collection (and all associated data)](actions/delete-a-collection-and-all-associated-data.md) | DELETE | Deletes a collection (and all associated data) from Weaviate. |
| [Delete a collection's vector index.](actions/delete-a-collections-vector-index.md) | DELETE | Deletes a collection's vector index from Weaviate. |
| [Delete a property's inverted index](actions/delete-a-propertys-inverted-index.md) | DELETE | Deletes a property's inverted index from Weaviate. |
| [Delete Collection](actions/delete-collection.md) | DELETE | Deletes a collection (and all associated data) from Weaviate. |
| [Get a single collection](actions/get-a-single-collection.md) | GET | Retrieves a single collection from Weaviate. |
| [Get Collection](actions/get-collection.md) | GET | Retrieves a single collection from Weaviate. |
| [Get Collection Shards](actions/get-collection-shards.md) | GET | Retrieves the shards status of a collection from Weaviate. |
| [Get the shards status of a collection](actions/get-the-shards-status-of-a-collection.md) | GET | Retrieves the shards status of a collection from Weaviate. |
| [List Collections](actions/list-collections.md) | GET | Retrieves all collection definitions from Weaviate. |
| [Delete a collection (and all associated data)](actions/schema-objects-delete.md) | DELETE | Deletes a collection (and all associated data) from Weaviate. |
| [Get a single collection](actions/schema-objects-get.md) | GET | Retrieves a single collection from Weaviate. |
| [Add a property to a collection](actions/schema-objects-properties-add.md) | POST | Adds a property to a collection in Weaviate. |
| [Delete a property's inverted index](actions/schema-objects-properties-delete.md) | DELETE | Deletes a property's inverted index from Weaviate. |
| [Tokenize text using a property's configuration](actions/schema-objects-properties-tokenize.md) | GET | Tokenizes text using a property's configuration in Weaviate. |
| [Get the shards status of a collection](actions/schema-objects-shards-get.md) | GET | Retrieves the shards status of a collection from Weaviate. |
| [Update a shard status](actions/schema-objects-shards-update.md) | PUT | Updates a shard status in Weaviate. |
| [Update collection definition](actions/schema-objects-update.md) | PUT | Updates collection definition in Weaviate. |
| [Delete a collection's vector index.](actions/schema-objects-vectors-delete.md) | DELETE | Deletes a collection's vector index from Weaviate. |
| [Tokenize text using a property's configuration](actions/tokenize-text-using-a-propertys-configuration.md) | GET | Tokenizes text using a property's configuration in Weaviate. |
| [Update a shard status](actions/update-a-shard-status.md) | PUT | Updates a shard status in Weaviate. |
| [Update collection definition](actions/update-collection-definition.md) | PUT | Updates collection definition in Weaviate. |

### Databases

| Action | Method | Description |
| --- | --- | --- |
| [Check Cluster Live](actions/check-cluster-live.md) | GET | Checks application liveness in Weaviate. |
| [Check Cluster Ready](actions/check-cluster-ready.md) | GET | Checks application readiness in Weaviate. |
| [Get cluster statistics](actions/cluster-get-statistics.md) | GET | Retrieves cluster statistics from Weaviate. |
| [Get Cluster Meta](actions/get-cluster-meta.md) | GET | Retrieves instance metadata from Weaviate. |
| [Get Cluster Nodes](actions/get-cluster-nodes.md) | GET | Retrieves node status from Weaviate. |
| [Get node status by collection](actions/get-node-status-by-collection.md) | GET | Retrieves node status by collection from Weaviate. |
| [Get node status by collection](actions/nodes-get-class.md) | GET | Retrieves node status by collection from Weaviate. |

### Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Get OIDC Configuration](actions/get-oidc-configuration.md) | GET | Retrieves OIDC configuration from Weaviate. |
| [List Available Endpoints](actions/list-available-endpoints.md) | GET | Retrieves available endpoints from Weaviate. |
| [Mcp.delete](actions/mcp-delete.md) | DELETE | Terminates an MCP session in Weaviate. |
| [Mcp.get](actions/mcp-get.md) | GET | Opens an MCP event stream in Weaviate. |
| [Mcp.post](actions/mcp-post.md) | GET | Handles MCP JSON-RPC requests in Weaviate. |

### Export Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Cancel an export](actions/export-cancel.md) | DELETE | Cancels an export in Weaviate. |
| [Start a new export](actions/export-create.md) | POST | Starts a new export in Weaviate. |
| [Get export status](actions/export-status.md) | GET | Retrieves export status from Weaviate. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Add Tenants](actions/add-tenants.md) | POST | Creates a new tenant in Weaviate. |
| [Assign a role to a group](actions/assignroletogroup.md) | PUT | Assigns a role to a group in Weaviate. |
| [Create a new tenant](actions/create-a-new-tenant.md) | POST | Creates a new tenant in Weaviate. |
| [Delete Tenants](actions/delete-tenants.md) | DELETE | Deletes tenants from Weaviate. |
| [Delete Tenants (Legacy Copy)](actions/delete-tenants-legacy-copy.md) | DELETE | Deletes tenants from Weaviate. |
| [Get a specific tenant](actions/get-a-specific-tenant.md) | GET | Retrieves a specific tenant from Weaviate. |
| [Get the list of tenants](actions/get-the-list-of-tenants.md) | GET | Retrieves the list of tenants from Weaviate. |
| [List all groups of a specific type](actions/getgroups.md) | GET | Retrieves all groups of a specific type from Weaviate. |
| [List all groups of a specific type](actions/list-all-groups-of-a-specific-type.md) | GET | Retrieves all groups of a specific type from Weaviate. |
| [List Tenants](actions/list-tenants.md) | GET | Retrieves the list of tenants from Weaviate. |
| [Revoke a role from a group](actions/revokerolefromgroup.md) | PUT | Revokes a role from a group in Weaviate. |
| [Create a new tenant](actions/tenants-create.md) | POST | Creates a new tenant in Weaviate. |
| [Delete tenants](actions/tenants-delete.md) | DELETE | Deletes tenants from Weaviate. |
| [Get the list of tenants](actions/tenants-get.md) | GET | Retrieves the list of tenants from Weaviate. |
| [Get a specific tenant](actions/tenants-get-one.md) | GET | Retrieves a specific tenant from Weaviate. |
| [Update a tenant](actions/tenants-update.md) | PUT | Updates a tenant in Weaviate. |
| [Update a tenant](actions/update-a-tenant.md) | PUT | Updates a tenant in Weaviate. |
| [Update Tenants](actions/update-tenants.md) | PUT | Updates a tenant in Weaviate. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Add an object reference](actions/add-an-object-reference.md) | POST | Adds an object reference in Weaviate. |
| [Add an Object Reference with Class Name (Legacy Copy)](actions/add-an-object-reference-with-class-name-legacy-copy.md) | POST | Adds an object reference in Weaviate. |
| [Add References Batch](actions/add-references-batch.md) | PUT | Creates cross-references in bulk in Weaviate. |
| [Create Object](actions/create-object.md) | POST | Creates an object in Weaviate. |
| [Create Objects Batch](actions/create-objects-batch.md) | POST | Creates objects in batch in Weaviate. |
| [Delete an object](actions/delete-an-object.md) | DELETE | Deletes an object from Weaviate. |
| [Delete an object reference](actions/delete-an-object-reference.md) | DELETE | Deletes an object reference from Weaviate. |
| [Delete an Object Reference with Class Name (Legacy Copy)](actions/delete-an-object-reference-with-class-name-legacy-copy.md) | DELETE | Deletes an object reference from Weaviate. |
| [Delete Object](actions/delete-object.md) | DELETE | Deletes an object from Weaviate. |
| [Delete Objects By Filter](actions/delete-objects-by-filter.md) | DELETE | Deletes objects in batch from Weaviate. |
| [Get an object](actions/get-an-object.md) | GET | Retrieves an object from Weaviate. |
| [Get Object](actions/get-object.md) | GET | Retrieves an object from Weaviate. |
| [List Objects](actions/list-objects.md) | GET | Retrieves objects from Weaviate. |
| [Delete an object](actions/objects-class-delete.md) | DELETE | Deletes an object from Weaviate. |
| [Get an object](actions/objects-class-get.md) | GET | Retrieves an object from Weaviate. |
| [Patch an object](actions/objects-class-patch.md) | PUT | Patches an object in Weaviate. |
| [Replace an object](actions/objects-class-put.md) | PUT | Replaces an object in Weaviate. |
| [Add an object reference](actions/objects-class-references-create.md) | POST | Adds an object reference in Weaviate. |
| [Delete an object reference](actions/objects-class-references-delete.md) | DELETE | Deletes an object reference from Weaviate. |
| [Replace object references](actions/objects-class-references-put.md) | PUT | Replaces object references in Weaviate. |
| [Delete an object](actions/objects-delete.md) | DELETE | Deletes an object from Weaviate. |
| [Get an object](actions/objects-get.md) | GET | Retrieves an object from Weaviate. |
| [Patch an object](actions/objects-patch.md) | PUT | Patches an object in Weaviate. |
| [Add an object reference](actions/objects-references-create.md) | POST | Adds an object reference in Weaviate. |
| [Delete an object reference](actions/objects-references-delete.md) | DELETE | Deletes an object reference from Weaviate. |
| [Replace object references](actions/objects-references-update.md) | PUT | Replaces object references in Weaviate. |
| [Update an object](actions/objects-update.md) | PUT | Updates an object in Weaviate. |
| [Validate an object](actions/objects-validate.md) | GET | Validates an object in Weaviate. |
| [Patch an object](actions/patch-an-object.md) | PUT | Patches an object in Weaviate. |
| [Replace an object](actions/replace-an-object.md) | PUT | Replaces an object in Weaviate. |
| [Replace Object](actions/replace-object.md) | PUT | Updates an object in Weaviate. |
| [Replace object references](actions/replace-object-references.md) | PUT | Replaces object references in Weaviate. |
| [Replace Object References with Class Name (Legacy Copy)](actions/replace-object-references-with-class-name-legacy-copy.md) | PUT | Replaces object references in Weaviate. |
| [Update Object](actions/update-object.md) | PUT | Patches an object in Weaviate. |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Cancel a backup](actions/backups-cancel.md) | DELETE | Cancels a backup in Weaviate. |
| [Create a backup](actions/backups-create.md) | POST | Creates a backup in Weaviate. |
| [Get backup creation status](actions/backups-create-status.md) | GET | Retrieves backup creation status from Weaviate. |
| [List all created backups](actions/backups-list.md) | GET | Retrieves all created backups from Weaviate. |
| [Restore from a backup](actions/backups-restore.md) | POST | Restores from a backup in Weaviate. |
| [Cancel a backup restoration](actions/backups-restore-cancel.md) | DELETE | Cancels a backup restoration in Weaviate. |
| [Get backup restoration status](actions/backups-restore-status.md) | GET | Retrieves backup restoration status from Weaviate. |
| [Get classification status](actions/classifications-get.md) | GET | Retrieves classification status from Weaviate. |
| [Start a classification](actions/classifications-post.md) | POST | Starts a classification in Weaviate. |

### Labels

| Action | Method | Description |
| --- | --- | --- |
| [Create a new alias](actions/aliases-create.md) | POST | Creates a new alias in Weaviate. |
| [Delete an alias](actions/aliases-delete.md) | DELETE | Deletes an alias from Weaviate. |
| [List aliases](actions/aliases-get.md) | GET | Retrieves aliases from Weaviate. |
| [Get an alias](actions/aliases-get-alias.md) | GET | Retrieves an alias from Weaviate. |
| [Update an alias](actions/aliases-update.md) | PUT | Updates an alias in Weaviate. |
| [Delete an alias](actions/delete-an-alias.md) | DELETE | Deletes an alias from Weaviate. |
| [Get an alias](actions/get-an-alias.md) | GET | Retrieves an alias from Weaviate. |
| [Update an alias](actions/update-an-alias.md) | PUT | Updates an alias in Weaviate. |

### Queries

| Action | Method | Description |
| --- | --- | --- |
| [Perform batched GraphQL queries](actions/graphql-batch.md) | GET | Runs batched GraphQL queries in Weaviate. |
| [Run GraphQL Query](actions/run-graph-ql-query.md) | GET | Runs a GraphQL query in Weaviate. |
| [Tokenize text](actions/tokenize.md) | GET | Tokenizes text in Weaviate. |

### Roles

| Action | Method | Description |
| --- | --- | --- |
| [Add permissions to a role](actions/add-permissions-to-a-role.md) | POST | Adds permissions to a role in Weaviate. |
| [Add permissions to a role](actions/addpermissions.md) | PUT | Adds permissions to a role in Weaviate. |
| [Create new role](actions/createrole.md) | POST | Creates a new role in Weaviate. |
| [Delete a role](actions/deleterole.md) | DELETE | Deletes a role from Weaviate. |
| [Get groups that have a specific role assigned](actions/get-groups-that-have-a-specific-role-assigned.md) | GET | Retrieves groups that have a specific role assigned from Weaviate. |
| [Get roles assigned to a specific group](actions/get-roles-assigned-to-a-specific-group.md) | GET | Retrieves roles assigned to a specific group from Weaviate. |
| [Get roles assigned to a user](actions/get-roles-assigned-to-a-user.md) | GET | Retrieves roles assigned to a user from Weaviate. |
| [Get Roles Assigned to a User (Legacy Copy)](actions/get-roles-assigned-to-a-user-legacy-copy.md) | GET | Retrieves roles assigned to a user from Weaviate. |
| [Get users assigned to a role](actions/get-users-assigned-to-a-role.md) | GET | Retrieves users assigned to a role from Weaviate. |
| [Get Users Assigned to a Role (Legacy Copy)](actions/get-users-assigned-to-a-role-legacy-copy.md) | GET | Retrieves users assigned to a role from Weaviate. |
| [Get groups that have a specific role assigned](actions/getgroupsforrole.md) | GET | Retrieves groups that have a specific role assigned from Weaviate. |
| [Get a role](actions/getrole.md) | GET | Retrieves a role from Weaviate. |
| [Get all roles](actions/getroles.md) | GET | Retrieves all roles from Weaviate. |
| [Get roles assigned to a specific group](actions/getrolesforgroup.md) | GET | Retrieves roles assigned to a specific group from Weaviate. |
| [Get roles assigned to a user](actions/getrolesforuser.md) | GET | Retrieves roles assigned to a user from Weaviate. |
| [Get roles assigned to a user](actions/getrolesforuserdeprecated.md) | GET | Retrieves roles assigned to a user from Weaviate. |
| [Get users assigned to a role](actions/getusersforrole.md) | GET | Retrieves users assigned to a role from Weaviate. |
| [Get users assigned to a role](actions/getusersforroledeprecated.md) | GET | Retrieves users assigned to a role from Weaviate. |
| [Check whether a role possesses a permission](actions/haspermission.md) | GET | Checks whether a role possesses a permission in Weaviate. |
| [Remove permissions from a role](actions/remove-permissions-from-a-role.md) | POST | Removes permissions from a role in Weaviate. |
| [Remove permissions from a role](actions/removepermissions.md) | PUT | Removes permissions from a role in Weaviate. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Apply replication scaling plan](actions/applyreplicationscaleplan.md) | PUT | Applies replication scaling plan in Weaviate. |
| [Cancel a replication operation](actions/cancelreplication.md) | PUT | Cancels a replication operation in Weaviate. |
| [Delete all replication operations](actions/deleteallreplications.md) | DELETE | Deletes all replication operations from Weaviate. |
| [Delete a replication operation](actions/deletereplication.md) | DELETE | Deletes a replication operation from Weaviate. |
| [Lists all distributed tasks in the cluster](actions/distributedtasks-get.md) | GET | Lists all distributed tasks in the cluster in Weaviate. |
| [Force delete replication operations](actions/forcedeletereplications.md) | POST | Force deletes replication operations in Weaviate. |
| [Get sharding state](actions/getcollectionshardingstate.md) | GET | Retrieves sharding state from Weaviate. |
| [Get replication scale plan](actions/getreplicationscaleplan.md) | GET | Retrieves replication scale plan from Weaviate. |
| [List replication operations](actions/listreplication.md) | GET | Retrieves replication operations from Weaviate. |
| [Initiate a replica movement](actions/replicate.md) | POST | Initiates a replica movement in Weaviate. |
| [Retrieve a replication operation](actions/replicationdetails.md) | GET | Retrieve a replication operation in Weaviate. |
| [Retrieve a replication operation](actions/retrieve-a-replication-operation.md) | GET | Retrieve a replication operation in Weaviate. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Activate a user](actions/activate-a-user.md) | PUT | Activates a user in Weaviate. |
| [Activate a user](actions/activateuser.md) | PUT | Activates a user in Weaviate. |
| [Assign a role to a user](actions/assignroletouser.md) | PUT | Assigns a role to a user in Weaviate. |
| [Create a new user](actions/create-a-new-user.md) | POST | Creates a new user in Weaviate. |
| [Create a new user](actions/createuser.md) | POST | Creates a new user in Weaviate. |
| [Deactivate a user](actions/deactivate-a-user.md) | PUT | Deactivates a user in Weaviate. |
| [Deactivate a user](actions/deactivateuser.md) | PUT | Deactivates a user in Weaviate. |
| [Delete a user](actions/delete-a-user.md) | DELETE | Deletes a user from Weaviate. |
| [Delete a user](actions/deleteuser.md) | DELETE | Deletes a user from Weaviate. |
| [Get User Info (Lowercase User ID)](actions/get-user-info-lowercase-user-id.md) | GET | Retrieves user info from Weaviate. |
| [Get current user info](actions/getowninfo.md) | GET | Retrieves current user info from Weaviate. |
| [Get user info](actions/getuserinfo.md) | GET | Retrieves user info from Weaviate. |
| [List all users](actions/listallusers.md) | GET | Retrieves all users from Weaviate. |
| [Revoke a role from a user](actions/revokerolefromuser.md) | PUT | Revokes a role from a user in Weaviate. |
| [Rotate API key of a user](actions/rotate-api-key-of-a-user.md) | PUT | Rotates API key of a user in Weaviate. |
| [Rotate API key of a user](actions/rotateuserapikey.md) | PUT | Rotates API key of a user in Weaviate. |

