# Database management

You can add and remove databases, as well as view information about them.

## Getting a list of cluster databases {#list-db}

{% list tabs %}

- Management console
  1. Go to the folder page and select **{{ mch-name }}**.
  1. Click on the name of the cluster you need and select the **Databases** tab.

- CLI

  {% include [cli-install](../../_includes/cli-install.md) %}

  {% include [default-catalogue](../../_includes/default-catalogue.md) %}

  To get a list of databases in a cluster, run the command:

  ```
  $ yc managed-clickhouse database list
       --cluster-name=<cluster name>
  ```

  The cluster name can be requested with a [list of folder clusters](#list-clusters).

- API

  To get a list of cluster databases, use the [list](../api-ref/Database/list.md) method.

{% endlist %}

## Creating a database {#add-db}

The number of databases in a cluster is unlimited.

{% list tabs %}

- Management console
  1. Go to the folder page and select **{{ mch-name }}**.
  1. Click on the name of the cluster you need.
  1. Select the **Databases** tab.
  1. Click **Add**.
  1. Enter the DB name and click **Add**.

- CLI

  {% include [cli-install](../../_includes/cli-install.md) %}

  {% include [default-catalogue](../../_includes/default-catalogue.md) %}

  Run the create database command and set the name of the new database:

  ```
  $ yc managed-clickhouse  database create <database name>
      --cluster-name <cluster name>
  ```

  {{ mch-short-name }} runs the create database operation.

  The cluster name can be requested with a [list of folder clusters](#list-clusters).

- API

  You can create a new database in a cluster using the [create](../api-ref/Database/create.md) method.

{% endlist %}

## Deleting a database {#remove-db}

{% list tabs %}

- Management console
  1. Go to the folder page and select **{{ mch-name }}**.
  1. Click on the name of the cluster you need and select the **Databases** tab.
  1. Click ![image](../../_assets/vertical-ellipsis.svg) in the line of the necessary DB and select **Delete**.

- CLI

  {% include [cli-install](../../_includes/cli-install.md) %}

  {% include [default-catalogue](../../_includes/default-catalogue.md) %}

  To delete a database, run the command:

  ```
  $ yc managed-clickhouse database delete <database name>
       --cluster-name=<cluster name>
  ```

  The cluster name can be requested with a [list of folder clusters](#list-clusters).

- API

  You can delete a database using the [delete](../api-ref/Database/delete.md) method.

{% endlist %}
