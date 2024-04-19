# `khulnasoft/wrappers`

<p>
<a href=""><img src="https://img.shields.io/badge/postgresql-14+-blue.svg" alt="PostgreSQL version" height="18"></a>
<a href="https://github.com/khulnasoft/wrappers/blob/master/LICENSE"><img src="https://img.shields.io/pypi/l/markdown-subtemplate.svg" alt="License" height="18"></a>
<a href="https://github.com/khulnasoft/wrappers/actions"><img src="https://github.com/khulnasoft/wrappers/actions/workflows/test_wrappers.yml/badge.svg" alt="Tests" height="18"></a>

</p>

---

**Documentation**: <a href="https://khulnasoft.github.io/wrappers" target="_blank">https://khulnasoft.github.io/wrappers</a>

**Source Code**: <a href="https://github.com/khulnasoft/wrappers" target="_blank">https://github.com/khulnasoft/wrappers</a>

---

## Overview

`khulnasoft/wrappers` is a PostgreSQL extension that provides integrations with external sources so you can interact with third-party data using SQL.

For example, the Stripe wrapper allows you to query and join against your Stripe customer data straight from PostgreSQL:

```sql
select
  customer_id
  currency
from
   stripe.customers;
```

returns

```
    customer_id     | currency
--------------------+-----------
 cus_MJiBtCqOF1Bb3F | usd
(1 row)
```

Currently `khulnasoft/wrappers` supports:

| Integration | Select | Insert | Update | Delete | Truncate |
| ----------- | :----: | :----: | :----: | :----: | :------: |
| Airtable    |   ✅   |   ❌   |   ❌   |   ❌   |    ❌    |
| BigQuery    |   ✅   |   ✅   |   ✅   |   ✅   |    ❌    |
| ClickHouse  |   ✅   |   ✅   |   ✅   |   ✅   |    ❌    |
| Firebase    |   ✅   |   ❌   |   ❌   |   ❌   |    ❌    |
| Logflare    |   ✅   |   ❌   |   ❌   |   ❌   |    ❌    |
| Redis       |   ✅   |   ❌   |   ❌   |   ❌   |    ❌    |
| S3          |   ✅   |   ❌   |   ❌   |   ❌   |    ❌    |
| Stripe      |   ✅   |   ✅   |   ✅   |   ✅   |    ❌    |
| SQL Server  |   ✅   |   ❌   |   ❌   |   ❌   |    ❌    |
