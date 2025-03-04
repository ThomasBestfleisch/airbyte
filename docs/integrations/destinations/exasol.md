# Exasol

TODO: update this doc

## Sync overview

### Output schema

Is the output schema fixed (e.g: for an API like Stripe)? If so, point to the connector's schema (e.g: link to Stripe’s documentation) or describe the schema here directly (e.g: include a diagram or paragraphs describing the schema).

Describe how the connector's schema is mapped to Airbyte concepts. An example description might be: "MagicDB tables become Airbyte Streams and MagicDB columns become Airbyte Fields. In addition, an extracted\_at column is appended to each row being read."

### Data type mapping

This section should contain a table mapping each of the connector's data types to Airbyte types. At the moment, Airbyte uses the same types used by [JSONSchema](https://json-schema.org/understanding-json-schema/reference/index.html). `string`, `date-time`, `object`, `array`, `boolean`, `integer`, and `number` are the most commonly used data types.

| Integration Type | Airbyte Type | Notes |
| :--- | :--- | :--- |


### Features

This section should contain a table with the following format:

| Feature | Supported?(Yes/No) | Notes |
| :--- | :--- | :--- |
| Full Refresh Sync |  |  |
| Incremental Sync |  |  |
| Replicate Incremental Deletes |  |  |
| For databases, WAL/Logical replication |  |  |
| SSL connection |  |  |
| SSH Tunnel Support |  |  |
| (Any other source-specific features) |  |  |

### Performance considerations

Could this connector hurt the user's database/API/etc... or put too much strain on it in certain circumstances? For example, if there are a lot of tables or rows in a table? What is the breaking point (e.g: 100mm&gt; records)? What can the user do to prevent this? (e.g: use a read-only replica, or schedule frequent syncs, etc..)

## Getting started

### Requirements

* What versions of this connector does this implementation support? (e.g: `postgres v3.14 and above`)
* What configurations, if any, are required on the connector? (e.g: `buffer_size > 1024`)
* Network accessibility requirements
* Credentials/authentication requirements? (e.g: A  DB user with read permissions on certain tables)

### Setup guide

For each of the above high-level requirements as appropriate, add or point to a follow-along guide. See existing source or destination guides for an example.

For each major cloud provider we support, also add a follow-along guide for setting up Airbyte to connect to that destination. See the Postgres destination guide for an example of what this should look like.
