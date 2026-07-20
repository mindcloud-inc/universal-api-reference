# <img src="https://images.mindcloud.co/apps/icons/upstash-redis-icon_1776264343436.png" alt="Upstash Redis logo" width="28" height="28"> Upstash Redis: Universal API

Access Upstash Redis databases over the Upstash REST API, including generic Redis command execution, pipelines, atomic transactions, monitoring, and pub/sub operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/upstashRedis/latest
- **Category:** IT Operations / Database
- **Actions:** 257
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://upstash.com
- **Vendor API docs:** https://upstash.com/docs/redis/features/restapi

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Ping](actions/ping.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upstashRedis/latest/actions/ping?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (257)

### Channel

| Action | Method | Description |
| --- | --- | --- |
| [Publish Message](actions/publish-message.md) | POST | Publishes a message to an Upstash Redis channel. |

### Database

| Action | Method | Description |
| --- | --- | --- |
| [ACL](actions/acl.md) | POST | Executes the ACL command in Upstash Redis to manage access control list. |
| [APPEND](actions/append.md) | POST | Executes the APPEND command in Upstash Redis to append value to a string. |
| [AUTH](actions/auth.md) | POST |  |
| [BITCOUNT](actions/bitcount.md) | GET | Executes the BITCOUNT command in Upstash Redis to count set bits in a string. |
| [BITFIELD](actions/bitfield.md) | POST | Executes the BITFIELD command in Upstash Redis to perform arbitrary bitfield operations. |
| [BITFIELD_RO](actions/bitfield-ro.md) | GET | Executes the BITFIELD_RO command in Upstash Redis to read-only bitfield operations. |
| [BITOP](actions/bitop.md) | POST | Executes the BITOP command in Upstash Redis to perform bitwise operations between strings. |
| [BITPOS](actions/bitpos.md) | GET | Finds the first set or clear bit in Upstash Redis. |
| [BLMOVE](actions/blmove.md) | POST | Executes the BLMOVE command in Upstash Redis to blocking list move. |
| [BLMPOP](actions/blmpop.md) | POST | Executes the BLMPOP command in Upstash Redis to blocking pop from multiple lists. |
| [BLPOP](actions/blpop.md) | POST |  |
| [BRPOP](actions/brpop.md) | POST |  |
| [BRPOPLPUSH](actions/brpoplpush.md) | POST |  |
| [BZMPOP](actions/bzmpop.md) | POST | Executes the BZMPOP command in Upstash Redis to blocking pop from sorted sets. |
| [BZPOPMAX](actions/bzpopmax.md) | POST |  |
| [BZPOPMIN](actions/bzpopmin.md) | POST |  |
| [CLIENT GETNAME](actions/client-getname.md) | GET |  |
| [CLIENT ID](actions/client-id.md) | GET |  |
| [CLIENT INFO](actions/client-info.md) | GET |  |
| [CLIENT LIST](actions/client-list.md) | GET |  |
| [CLIENT SETINFO](actions/client-setinfo.md) | POST |  |
| [CLIENT SETNAME](actions/client-setname.md) | POST |  |
| [COPY](actions/copy.md) | POST | Executes the COPY command in Upstash Redis to copy a key to another key. |
| [DBSIZE](actions/dbsize.md) | GET | Executes the DBSIZE command in Upstash Redis to get number of keys in database. |
| [DECR](actions/decr.md) | POST | Executes the DECR command in Upstash Redis to decrement integer value by 1. |
| [DECRBY](actions/decrby.md) | POST | Executes the DECRBY command in Upstash Redis to decrement integer by amount. |
| [DEL](actions/del.md) | DELETE | Executes the DEL command in Upstash Redis to delete one or more keys. |
| [DISCARD](actions/discard.md) | POST |  |
| [DUMP](actions/dump.md) | POST | Executes the DUMP command in Upstash Redis to serialize a key’s value. |
| [ECHO](actions/echo.md) | GET | Executes the ECHO command in Upstash Redis to echo the given string. |
| [EVAL](actions/eval.md) | POST | Executes the EVAL command in Upstash Redis to execute a Lua script. |
| [EVAL_RO](actions/eval-ro.md) | POST | Executes the EVAL_RO command in Upstash Redis to execute read-only Lua script. |
| [EVALSHA](actions/evalsha.md) | POST | Executes the EVALSHA command in Upstash Redis to execute cached Lua script by SHA. |
| [EVALSHA_RO](actions/evalsha-ro.md) | POST | Executes the EVALSHA_RO command in Upstash Redis to read-only execute by SHA. |
| [EXEC](actions/exec.md) | POST | Executes the EXEC command in Upstash Redis to execute queued commands. |
| [EXISTS](actions/exists.md) | GET | Executes the EXISTS command in Upstash Redis to check if keys exist. |
| [EXPIRE](actions/expire.md) | POST | Executes the EXPIRE command in Upstash Redis to set a key’s TTL in seconds. |
| [EXPIREAT](actions/expireat.md) | POST | Executes the EXPIREAT command in Upstash Redis to set expiry as Unix timestamp. |
| [EXPIRETIME](actions/expiretime.md) | GET | Executes the EXPIRETIME command in Upstash Redis to get expiry as Unix timestamp. |
| [FCALL](actions/fcall.md) | POST | Executes the FCALL command in Upstash Redis to call a function. |
| [FCALL_RO](actions/fcall-ro.md) | POST | Executes the FCALL_RO command in Upstash Redis to call a read-only function. |
| [FLUSHALL](actions/flushall.md) | POST | Executes the FLUSHALL command in Upstash Redis to delete all keys in all databases. |
| [FLUSHDB](actions/flushdb.md) | POST | Executes the FLUSHDB command in Upstash Redis to delete all keys in current database. |
| [FUNCTION DELETE](actions/function-delete.md) | DELETE | Executes the FUNCTION DELETE command in Upstash Redis to delete a library. |
| [FUNCTION FLUSH](actions/function-flush.md) | DELETE | Executes the FUNCTION FLUSH command in Upstash Redis to delete all libraries. |
| [FUNCTION KILL](actions/function-kill.md) | POST | Executes the FUNCTION KILL command in Upstash Redis to kill a running function. |
| [FUNCTION LIST](actions/function-list.md) | GET | Executes the FUNCTION LIST command in Upstash Redis to list all libraries. |
| [FUNCTION LOAD](actions/function-load.md) | POST | Executes the FUNCTION LOAD command in Upstash Redis to load a library. |
| [FUNCTION STATS](actions/function-stats.md) | GET | Executes the FUNCTION STATS command in Upstash Redis to get function execution stats. |
| [GEOADD](actions/geoadd.md) | POST | Executes the GEOADD command in Upstash Redis to add geospatial items. |
| [GEODIST](actions/geodist.md) | GET | Executes the GEODIST command in Upstash Redis to get distance between two members. |
| [GEOHASH](actions/geohash.md) | GET | Executes the GEOHASH command in Upstash Redis to get geohash strings for members. |
| [GEOPOS](actions/geopos.md) | GET | Executes the GEOPOS command in Upstash Redis to get coordinates of members. |
| [GEORADIUS](actions/georadius.md) | GET | Executes the GEORADIUS command in Upstash Redis to query members within radius. |
| [GEORADIUS_RO](actions/georadius-ro.md) | GET | Executes the GEORADIUS_RO command in Upstash Redis to read-only radius query. |
| [GEORADIUSBYMEMBER](actions/georadiusbymember.md) | GET | Executes the GEORADIUSBYMEMBER command in Upstash Redis to radius query centered on member. |
| [GEORADIUSBYMEMBER_RO](actions/georadiusbymember-ro.md) | GET | Executes the GEORADIUSBYMEMBER_RO command in Upstash Redis to read-only radius query by member. |
| [GEOSEARCH](actions/geosearch.md) | GET | Executes the GEOSEARCH command in Upstash Redis to search for members in an area. |
| [GEOSEARCHSTORE](actions/geosearchstore.md) | POST | Executes the GEOSEARCHSTORE command in Upstash Redis to store geosearch results. |
| [GET](actions/get.md) | GET | Executes the GET command in Upstash Redis to get string value. |
| [Get Database Info](actions/get-database-info.md) | GET | Retrieves database info from Upstash Redis. |
| [GETBIT](actions/getbit.md) | GET | Executes the GETBIT command in Upstash Redis to get the bit value at offset. |
| [GETDEL](actions/getdel.md) | GET | Executes the GETDEL command in Upstash Redis to get value and delete key. |
| [GETEX](actions/getex.md) | GET | Executes the GETEX command in Upstash Redis to get value and set expiration. |
| [GETRANGE](actions/getrange.md) | GET | Executes the GETRANGE command in Upstash Redis to get substring of string. |
| [GETSET](actions/getset.md) | GET | Executes the GETSET command in Upstash Redis to set value and return old value. |
| [HDEL](actions/hdel.md) | DELETE | Executes the HDEL command in Upstash Redis to delete one or more hash fields. |
| [HELLO](actions/hello.md) | GET |  |
| [HEXISTS](actions/hexists.md) | GET | Executes the HEXISTS command in Upstash Redis to check if a hash field exists. |
| [HEXPIRE](actions/hexpire.md) | POST | Executes the HEXPIRE command in Upstash Redis to set field TTL in seconds. |
| [HEXPIREAT](actions/hexpireat.md) | POST | Executes the HEXPIREAT command in Upstash Redis to set field expiry as timestamp. |
| [HEXPIRETIME](actions/hexpiretime.md) | GET | Executes the HEXPIRETIME command in Upstash Redis to get field expiry as timestamp. |
| [HGET](actions/hget.md) | GET | Gets a hash field value from Upstash Redis. |
| [HGETALL](actions/hgetall.md) | GET | Executes the HGETALL command in Upstash Redis to get all fields and values. |
| [HGETDEL](actions/hgetdel.md) | GET | Executes the HGETDEL command in Upstash Redis to get and delete hash fields. |
| [HGETEX](actions/hgetex.md) | GET | Executes the HGETEX command in Upstash Redis to get fields and set their expiry. |
| [HINCRBY](actions/hincrby.md) | POST | Executes the HINCRBY command in Upstash Redis to increment integer value of a field. |
| [HINCRBYFLOAT](actions/hincrbyfloat.md) | POST | Executes the HINCRBYFLOAT command in Upstash Redis to increment float value of a field. |
| [HKEYS](actions/hkeys.md) | GET | Executes the HKEYS command in Upstash Redis to get all fields in a hash. |
| [HLEN](actions/hlen.md) | GET | Gets the number of fields in an Upstash Redis hash. |
| [HMGET](actions/hmget.md) | GET | Executes the HMGET command in Upstash Redis to get values of multiple fields. |
| [HMSET](actions/hmset.md) | POST | Executes the HMSET command in Upstash Redis to set multiple hash fields. |
| [HPERSIST](actions/hpersist.md) | POST | Executes the HPERSIST command in Upstash Redis to remove field expiration. |
| [HPEXPIRE](actions/hpexpire.md) | POST | Executes the HPEXPIRE command in Upstash Redis to set field TTL in milliseconds. |
| [HPEXPIREAT](actions/hpexpireat.md) | POST | Executes the HPEXPIREAT command in Upstash Redis to set field expiry as ms timestamp. |
| [HPEXPIRETIME](actions/hpexpiretime.md) | GET | Executes the HPEXPIRETIME command in Upstash Redis to get field expiry as ms timestamp. |
| [HPTTL](actions/hpttl.md) | GET | Executes the HPTTL command in Upstash Redis to get field TTL in milliseconds. |
| [HRANDFIELD](actions/hrandfield.md) | GET | Executes the HRANDFIELD command in Upstash Redis to get random fields from a hash. |
| [HSCAN](actions/hscan.md) | GET | Executes the HSCAN command in Upstash Redis to incrementally iterate hash fields. |
| [HSET](actions/hset.md) | POST | Executes the HSET command in Upstash Redis to set hash field values. |
| [HSETEX](actions/hsetex.md) | POST | Executes the HSETEX command in Upstash Redis to set fields with expiration. |
| [HSETNX](actions/hsetnx.md) | POST | Sets a hash field in Upstash Redis if absent. |
| [HSTRLEN](actions/hstrlen.md) | GET | Executes the HSTRLEN command in Upstash Redis to get length of a field’s value. |
| [HTTL](actions/httl.md) | GET | Executes the HTTL command in Upstash Redis to get field TTL in seconds. |
| [HVALS](actions/hvals.md) | GET | Executes the HVALS command in Upstash Redis to get all values in a hash. |
| [INCR](actions/incr.md) | POST | Executes the INCR command in Upstash Redis to increment integer value by 1. |
| [INCRBY](actions/incrby.md) | POST | Executes the INCRBY command in Upstash Redis to increment integer by amount. |
| [INCRBYFLOAT](actions/incrbyfloat.md) | POST | Executes the INCRBYFLOAT command in Upstash Redis to increment float by amount. |
| [JSON.ARRAPPEND](actions/json-arrappend.md) | POST | Executes the JSON.ARRAPPEND command in Upstash Redis to append values to JSON array. |
| [JSON.ARRINDEX](actions/json-arrindex.md) | POST | Executes the JSON.ARRINDEX command in Upstash Redis to find index of value in array. |
| [JSON.ARRINSERT](actions/json-arrinsert.md) | POST | Executes the JSON.ARRINSERT command in Upstash Redis to insert values into JSON array. |
| [JSON.ARRLEN](actions/json-arrlen.md) | POST | Executes the JSON.ARRLEN command in Upstash Redis to get JSON array length. |
| [JSON.ARRPOP](actions/json-arrpop.md) | POST | Executes the JSON.ARRPOP command in Upstash Redis to pop value from JSON array. |
| [JSON.ARRTRIM](actions/json-arrtrim.md) | POST | Executes the JSON.ARRTRIM command in Upstash Redis to trim JSON array to range. |
| [JSON.CLEAR](actions/json-clear.md) | POST | Executes the JSON.CLEAR command in Upstash Redis to clear JSON values. |
| [JSON.DEL](actions/json-del.md) | DELETE | Executes the JSON.DEL command in Upstash Redis to delete JSON values. |
| [JSON.FORGET](actions/json-forget.md) | DELETE | Executes the JSON.FORGET command in Upstash Redis to alias for JSON.DEL. |
| [JSON.GET](actions/json-get.md) | GET | Executes the JSON.GET command in Upstash Redis to get JSON values. |
| [JSON.MERGE](actions/json-merge.md) | POST | Executes the JSON.MERGE command in Upstash Redis to merge JSON values. |
| [JSON.MGET](actions/json-mget.md) | GET | Executes the JSON.MGET command in Upstash Redis to get values from multiple keys. |
| [JSON.MSET](actions/json-mset.md) | POST | Executes the JSON.MSET command in Upstash Redis to set values in multiple keys. |
| [JSON.NUMINCRBY](actions/json-numincrby.md) | POST | Executes the JSON.NUMINCRBY command in Upstash Redis to increment JSON number. |
| [JSON.NUMMULTBY](actions/json-nummultby.md) | POST | Executes the JSON.NUMMULTBY command in Upstash Redis to multiply JSON number. |
| [JSON.OBJKEYS](actions/json-objkeys.md) | GET | Executes the JSON.OBJKEYS command in Upstash Redis to get JSON object keys. |
| [JSON.OBJLEN](actions/json-objlen.md) | GET | Executes the JSON.OBJLEN command in Upstash Redis to get JSON object size. |
| [JSON.RESP](actions/json-resp.md) | GET | Executes the JSON.RESP command in Upstash Redis to get JSON in RESP format. |
| [JSON.SET](actions/json-set.md) | POST | Executes the JSON.SET command in Upstash Redis to set JSON value. |
| [JSON.STRAPPEND](actions/json-strappend.md) | POST | Executes the JSON.STRAPPEND command in Upstash Redis to append to JSON string. |
| [JSON.STRLEN](actions/json-strlen.md) | GET | Executes the JSON.STRLEN command in Upstash Redis to get JSON string length. |
| [JSON.TOGGLE](actions/json-toggle.md) | POST | Executes the JSON.TOGGLE command in Upstash Redis to toggle JSON boolean. |
| [JSON.TYPE](actions/json-type.md) | GET | Executes the JSON.TYPE command in Upstash Redis to get JSON value type. |
| [KEYS](actions/keys.md) | GET | Executes the KEYS command in Upstash Redis to find keys matching a pattern. |
| [LINDEX](actions/lindex.md) | GET | Executes the LINDEX command in Upstash Redis to get element by index. |
| [LINSERT](actions/linsert.md) | GET | Executes the LINSERT command in Upstash Redis to insert before or after pivot. |
| [LLEN](actions/llen.md) | GET | Executes the LLEN command in Upstash Redis to get list length. |
| [LMOVE](actions/lmove.md) | POST | Executes the LMOVE command in Upstash Redis to move element between lists. |
| [LMPOP](actions/lmpop.md) | POST | Executes the LMPOP command in Upstash Redis to pop from multiple lists. |
| [LPOP](actions/lpop.md) | DELETE | Executes the LPOP command in Upstash Redis to pop from list head. |
| [LPOS](actions/lpos.md) | GET | Executes the LPOS command in Upstash Redis to find element position. |
| [LPUSH](actions/lpush.md) | POST | Executes the LPUSH command in Upstash Redis to push to list head. |
| [LPUSHX](actions/lpushx.md) | POST | Executes the LPUSHX command in Upstash Redis to push to head if list exists. |
| [LRANGE](actions/lrange.md) | GET | Executes the LRANGE command in Upstash Redis to get range of elements. |
| [LREM](actions/lrem.md) | POST | Executes the LREM command in Upstash Redis to remove elements by value. |
| [LSET](actions/lset.md) | POST | Executes the LSET command in Upstash Redis to set element at index. |
| [LTRIM](actions/ltrim.md) | POST | Executes the LTRIM command in Upstash Redis to trim list to range. |
| [MGET](actions/mget.md) | GET | Executes the MGET command in Upstash Redis to get values of multiple keys. |
| [MONITOR](actions/monitor.md) | GET | Executes the MONITOR command in Upstash Redis to stream all commands received. |
| [MSET](actions/mset.md) | POST | Executes the MSET command in Upstash Redis to set multiple keys at once. |
| [MSETNX](actions/msetnx.md) | POST | Executes the MSETNX command in Upstash Redis to set multiple keys if none exist. |
| [MULTI](actions/multi.md) | POST | Executes the MULTI command in Upstash Redis to start a transaction. |
| [PERSIST](actions/persist.md) | POST | Executes the PERSIST command in Upstash Redis to remove the expiration from a key. |
| [PEXPIRE](actions/pexpire.md) | POST | Executes the PEXPIRE command in Upstash Redis to set a key’s TTL in milliseconds. |
| [PEXPIREAT](actions/pexpireat.md) | POST | Executes the PEXPIREAT command in Upstash Redis to set expiry as Unix ms timestamp. |
| [PEXPIRETIME](actions/pexpiretime.md) | GET | Executes the PEXPIRETIME command in Upstash Redis to get expiry as Unix ms timestamp. |
| [PFADD](actions/pfadd.md) | POST | Executes the PFADD command in Upstash Redis to add elements to HyperLogLog. |
| [PFCOUNT](actions/pfcount.md) | GET | Executes the PFCOUNT command in Upstash Redis to get estimated cardinality. |
| [PFMERGE](actions/pfmerge.md) | POST | Executes the PFMERGE command in Upstash Redis to merge multiple HyperLogLogs. |
| [Ping](actions/ping.md) | GET | Retrieves a ping response from Upstash Redis. |
| [PSETEX](actions/psetex.md) | POST | Executes the PSETEX command in Upstash Redis to set value with ms expiration. |
| [PSUBSCRIBE](actions/psubscribe.md) | GET | Executes the PSUBSCRIBE command in Upstash Redis to subscribe to pattern channels. |
| [PTTL](actions/pttl.md) | GET | Executes the PTTL command in Upstash Redis to get TTL in milliseconds. |
| [PUBLISH](actions/publish.md) | POST | Executes the PUBLISH command in Upstash Redis to publish message to channel. |
| [PUBSUB](actions/pubsub.md) | GET | Executes the PUBSUB command in Upstash Redis to inspect pub/sub state. |
| [PUNSUBSCRIBE](actions/punsubscribe.md) | GET | Executes the PUNSUBSCRIBE command in Upstash Redis to unsubscribe from patterns. |
| [QUIT](actions/quit.md) | POST |  |
| [RANDOMKEY](actions/randomkey.md) | GET | Executes the RANDOMKEY command in Upstash Redis to return a random key. |
| [RENAME](actions/rename.md) | POST | Executes the RENAME command in Upstash Redis to rename a key. |
| [RENAMENX](actions/renamenx.md) | POST | Renames a key in Upstash Redis if the target is absent. |
| [RESET](actions/reset.md) | POST |  |
| [RESTORE](actions/restore.md) | POST | Executes the RESTORE command in Upstash Redis to deserialize and restore a key. |
| [RPOP](actions/rpop.md) | DELETE | Executes the RPOP command in Upstash Redis to pop from list tail. |
| [RPOPLPUSH](actions/rpoplpush.md) | POST | Moves a list item from tail to head in Upstash Redis. |
| [RPUSH](actions/rpush.md) | POST | Executes the RPUSH command in Upstash Redis to push to list tail. |
| [RPUSHX](actions/rpushx.md) | POST | Executes the RPUSHX command in Upstash Redis to push to tail if list exists. |
| [SADD](actions/sadd.md) | POST | Executes the SADD command in Upstash Redis to add members to a set. |
| [SCAN](actions/scan.md) | GET | Executes the SCAN command in Upstash Redis to incrementally iterate keys. |
| [SCARD](actions/scard.md) | GET | Executes the SCARD command in Upstash Redis to get set cardinality. |
| [SCRIPT EXISTS](actions/script-exists.md) | GET | Checks whether cached scripts exist in Upstash Redis. |
| [SCRIPT FLUSH](actions/script-flush.md) | DELETE | Executes the SCRIPT FLUSH command in Upstash Redis to clear the script cache. |
| [SCRIPT LOAD](actions/script-load.md) | POST | Executes the SCRIPT LOAD command in Upstash Redis to load script into cache. |
| [SDIFF](actions/sdiff.md) | GET | Executes the SDIFF command in Upstash Redis to get set difference. |
| [SDIFFSTORE](actions/sdiffstore.md) | POST | Executes the SDIFFSTORE command in Upstash Redis to store set difference. |
| [SELECT](actions/select.md) | POST |  |
| [SET](actions/set.md) | POST | Executes the SET command in Upstash Redis to set string value. |
| [SETBIT](actions/setbit.md) | POST | Sets or clears a bit in Upstash Redis. |
| [SETEX](actions/setex.md) | POST | Executes the SETEX command in Upstash Redis to set value with expiration. |
| [SETNX](actions/setnx.md) | POST | Executes the SETNX command in Upstash Redis to set value if key doesn’t exist. |
| [SETRANGE](actions/setrange.md) | POST | Executes the SETRANGE command in Upstash Redis to overwrite part of string. |
| [SINTER](actions/sinter.md) | GET | Executes the SINTER command in Upstash Redis to get set intersection. |
| [SINTERCARD](actions/sintercard.md) | GET | Executes the SINTERCARD command in Upstash Redis to get intersection cardinality. |
| [SINTERSTORE](actions/sinterstore.md) | POST | Executes the SINTERSTORE command in Upstash Redis to store set intersection. |
| [SISMEMBER](actions/sismember.md) | GET | Executes the SISMEMBER command in Upstash Redis to check if member exists in set. |
| [SMEMBERS](actions/smembers.md) | GET | Executes the SMEMBERS command in Upstash Redis to get all set members. |
| [SMISMEMBER](actions/smismember.md) | GET | Executes the SMISMEMBER command in Upstash Redis to check multiple members. |
| [SMOVE](actions/smove.md) | POST | Executes the SMOVE command in Upstash Redis to move member between sets. |
| [SPOP](actions/spop.md) | DELETE | Executes the SPOP command in Upstash Redis to remove random members. |
| [SRANDMEMBER](actions/srandmember.md) | GET | Executes the SRANDMEMBER command in Upstash Redis to get random members. |
| [SREM](actions/srem.md) | POST | Executes the SREM command in Upstash Redis to remove members from a set. |
| [SSCAN](actions/sscan.md) | GET | Executes the SSCAN command in Upstash Redis to incrementally iterate set members. |
| [STRLEN](actions/strlen.md) | GET | Executes the STRLEN command in Upstash Redis to get string length. |
| [SUBSCRIBE](actions/subscribe.md) | GET | Executes the SUBSCRIBE command in Upstash Redis to subscribe to channels. |
| [SUNION](actions/sunion.md) | GET | Executes the SUNION command in Upstash Redis to get set union. |
| [SUNIONSTORE](actions/sunionstore.md) | POST | Executes the SUNIONSTORE command in Upstash Redis to store set union. |
| [TIME](actions/time.md) | GET | Executes the TIME command in Upstash Redis to get current server time. |
| [TOUCH](actions/touch.md) | POST | Executes the TOUCH command in Upstash Redis to update last access time of keys. |
| [TTL](actions/ttl.md) | GET | Executes the TTL command in Upstash Redis to get TTL in seconds. |
| [TYPE](actions/type.md) | GET | Executes the TYPE command in Upstash Redis to get the type of a key. |
| [UNLINK](actions/unlink.md) | DELETE | Executes the UNLINK command in Upstash Redis to delete keys asynchronously. |
| [UNSUBSCRIBE](actions/unsubscribe.md) | GET | Executes the UNSUBSCRIBE command in Upstash Redis to unsubscribe from channels. |
| [UNWATCH](actions/unwatch.md) | POST |  |
| [WATCH](actions/watch.md) | POST |  |
| [XACK](actions/xack.md) | POST | Executes the XACK command in Upstash Redis to acknowledge stream messages. |
| [XACKDEL](actions/xackdel.md) | POST | Executes the XACKDEL command in Upstash Redis to acknowledge and delete messages. |
| [XADD](actions/xadd.md) | POST | Executes the XADD command in Upstash Redis to add entry to stream. |
| [XAUTOCLAIM](actions/xautoclaim.md) | POST | Executes the XAUTOCLAIM command in Upstash Redis to auto-claim idle messages. |
| [XCLAIM](actions/xclaim.md) | POST | Executes the XCLAIM command in Upstash Redis to claim pending messages. |
| [XDEL](actions/xdel.md) | DELETE | Executes the XDEL command in Upstash Redis to delete stream entries. |
| [XDELEX](actions/xdelex.md) | DELETE | Executes the XDELEX command in Upstash Redis to delete entries with expiration. |
| [XGROUP](actions/xgroup.md) | POST | Executes the XGROUP command in Upstash Redis to manage consumer groups. |
| [XINFO CONSUMERS](actions/xinfo-consumers.md) | GET | Executes the XINFO CONSUMERS command in Upstash Redis to list group consumers. |
| [XINFO GROUPS](actions/xinfo-groups.md) | GET | Executes the XINFO GROUPS command in Upstash Redis to list stream groups. |
| [XINFO STREAM](actions/xinfo-stream.md) | GET | Executes the XINFO STREAM command in Upstash Redis to get stream info. |
| [XLEN](actions/xlen.md) | GET | Executes the XLEN command in Upstash Redis to get stream length. |
| [XPENDING](actions/xpending.md) | GET | Executes the XPENDING command in Upstash Redis to get pending messages info. |
| [XRANGE](actions/xrange.md) | GET | Executes the XRANGE command in Upstash Redis to get range of stream entries. |
| [XREAD](actions/xread.md) | POST | Executes the XREAD command in Upstash Redis to read stream entries. |
| [XREADGROUP](actions/xreadgroup.md) | POST | Executes the XREADGROUP command in Upstash Redis to read as consumer group. |
| [XREVRANGE](actions/xrevrange.md) | GET | Executes the XREVRANGE command in Upstash Redis to get range in reverse order. |
| [XTRIM](actions/xtrim.md) | POST | Executes the XTRIM command in Upstash Redis to trim stream to max length. |
| [ZADD](actions/zadd.md) | POST | Executes the ZADD command in Upstash Redis to add members with scores. |
| [ZCARD](actions/zcard.md) | GET | Executes the ZCARD command in Upstash Redis to get sorted set cardinality. |
| [ZCOUNT](actions/zcount.md) | GET | Executes the ZCOUNT command in Upstash Redis to count members in score range. |
| [ZDIFF](actions/zdiff.md) | GET | Executes the ZDIFF command in Upstash Redis to get sorted set difference. |
| [ZDIFFSTORE](actions/zdiffstore.md) | POST | Executes the ZDIFFSTORE command in Upstash Redis to store sorted set difference. |
| [ZINCRBY](actions/zincrby.md) | POST | Executes the ZINCRBY command in Upstash Redis to increment member’s score. |
| [ZINTER](actions/zinter.md) | POST | Executes the ZINTER command in Upstash Redis to get sorted set intersection. |
| [ZINTERCARD](actions/zintercard.md) | POST | Executes the ZINTERCARD command in Upstash Redis to get intersection cardinality. |
| [ZINTERSTORE](actions/zinterstore.md) | POST | Executes the ZINTERSTORE command in Upstash Redis to store sorted set intersection. |
| [ZLEXCOUNT](actions/zlexcount.md) | GET | Executes the ZLEXCOUNT command in Upstash Redis to count members in lex range. |
| [ZMPOP](actions/zmpop.md) | POST | Executes the ZMPOP command in Upstash Redis to pop members from sorted sets. |
| [ZMSCORE](actions/zmscore.md) | GET | Executes the ZMSCORE command in Upstash Redis to get scores of multiple members. |
| [ZPOPMAX](actions/zpopmax.md) | DELETE | Executes the ZPOPMAX command in Upstash Redis to pop members with highest scores. |
| [ZPOPMIN](actions/zpopmin.md) | DELETE | Executes the ZPOPMIN command in Upstash Redis to pop members with lowest scores. |
| [ZRANDMEMBER](actions/zrandmember.md) | GET | Executes the ZRANDMEMBER command in Upstash Redis to get random members. |
| [ZRANGE](actions/zrange.md) | GET | Executes the ZRANGE command in Upstash Redis to get members by index range. |
| [ZRANGEBYLEX](actions/zrangebylex.md) | GET | Executes the ZRANGEBYLEX command in Upstash Redis to get members by lex range. |
| [ZRANGEBYSCORE](actions/zrangebyscore.md) | GET | Executes the ZRANGEBYSCORE command in Upstash Redis to get members by score range. |
| [ZRANGESTORE](actions/zrangestore.md) | POST | Executes the ZRANGESTORE command in Upstash Redis to store range result. |
| [ZRANK](actions/zrank.md) | GET | Executes the ZRANK command in Upstash Redis to get member’s rank. |
| [ZREM](actions/zrem.md) | POST | Executes the ZREM command in Upstash Redis to remove members. |
| [ZREMRANGEBYLEX](actions/zremrangebylex.md) | POST | Executes the ZREMRANGEBYLEX command in Upstash Redis to remove members by lex range. |
| [ZREMRANGEBYRANK](actions/zremrangebyrank.md) | POST | Executes the ZREMRANGEBYRANK command in Upstash Redis to remove members by rank range. |
| [ZREMRANGEBYSCORE](actions/zremrangebyscore.md) | POST | Executes the ZREMRANGEBYSCORE command in Upstash Redis to remove members by score range. |
| [ZREVRANGE](actions/zrevrange.md) | GET | Executes the ZREVRANGE command in Upstash Redis to get members in reverse order. |
| [ZREVRANGEBYLEX](actions/zrevrangebylex.md) | GET | Executes the ZREVRANGEBYLEX command in Upstash Redis to reverse lex range query. |
| [ZREVRANGEBYSCORE](actions/zrevrangebyscore.md) | GET | Executes the ZREVRANGEBYSCORE command in Upstash Redis to reverse score range query. |
| [ZREVRANK](actions/zrevrank.md) | GET | Executes the ZREVRANK command in Upstash Redis to get member’s reverse rank. |
| [ZSCAN](actions/zscan.md) | GET | Executes the ZSCAN command in Upstash Redis to incrementally iterate sorted set. |
| [ZSCORE](actions/zscore.md) | GET | Executes the ZSCORE command in Upstash Redis to get member’s score. |
| [ZUNION](actions/zunion.md) | POST | Executes the ZUNION command in Upstash Redis to get sorted set union. |
| [ZUNIONSTORE](actions/zunionstore.md) | POST | Executes the ZUNIONSTORE command in Upstash Redis to store sorted set union. |

### Key

| Action | Method | Description |
| --- | --- | --- |
| [Check Key Exists](actions/check-key-exists.md) | GET | Checks whether a key exists in Upstash Redis. |
| [Delete Key](actions/delete-key.md) | DELETE | Deletes a key from Upstash Redis. |
| [Get Key TTL](actions/get-key-ttl.md) | GET | Retrieves a key TTL from Upstash Redis. |
| [Get Key Value](actions/get-key-value.md) | GET | Retrieves a key value from Upstash Redis. |
| [Set Key Value](actions/set-key-value.md) | POST | Sets a key value in Upstash Redis. |

