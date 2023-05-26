Welcome to your new dbt project!

### Using the starter project

Try running the following commands:
- dbt run
- dbt test


### Resources:
- Learn more about dbt [in the docs](https://docs.getdbt.com/docs/introduction)
- Check out [Discourse](https://discourse.getdbt.com/) for commonly asked questions and answers
- Join the [dbt community](http://community.getbdt.com/) to learn from other analytics engineers
- Find [dbt events](https://events.getdbt.com) near you
- Check out [the blog](https://blog.getdbt.com/) for the latest news on dbt's development and best practices


Snowfalke setups

```
CREATE DATABSE analytics;

create warehouse transforming with warehouse_size='MEDIUM';

create role transformer;

grant IMPORTED PRIVILEGES on database snowflake_sample_data to role transformer;
grant usage on schema snowflake_sample_data.tpch_sf10 to role transformer;
grant select on all tables in schema snowflake_sample_data.tpch_sf10 to role transformer;

grant usage on database analytics to role transformer;
grant modify on database analytics to role transformer;
grant monitor on database analytics to role transformer;
grant create schema on database analytics to role transformer;

grant operate on warehouse transforming to role transformer;
grant usage on warehouse transforming to role transformer;

```