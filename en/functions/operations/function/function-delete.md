# Deleting a function

{% include [function-list-note](../../../_includes/functions/function-list-note.md) %}

## Deleting a function

{% list tabs %}

- Management console

   To delete a [function](../../concepts/function.md):
   1. In the [management console]({{ link-console-main }}), select the folder from which you wish to delete the function.
   1. Select **{{ sf-name }}**.
   1. In the line of the function, click ![image](../../../_assets/options.svg) and select **Delete**.
   1. In the window that opens, click **Delete**.

- CLI

   {% include [cli-install](../../../_includes/cli-install.md) %}

   Delete the function:

   ```
   yc serverless function delete <function name>
   ```
   Result:
   ```
   done (1s)    
   id: b09kk2ujb8js23f73b06
   folder_id: aoek49ghmknnpj1ll45e
   created_at: "2019-06-13T13:21:40.022Z"
   name: my-functions
   log_group_id: eolq9ac97486t34iut5q
   http_invoke_url: https://functions.yandexcloud.net/b09kk2ujb8js23f73b06
   status: DELETING
   ```

- Terraform

   {% include [terraform-definition](../../../_tutorials/terraform-definition.md) %}

   For more on Terraform, [review the documentation](../../../tutorials/infrastructure-management/terraform-quickstart.md#install-terraform).

   If you created a function using Terraform, you can delete it:

   1. In the command line, go to the directory with the Terraform configuration file.
   1. Delete resources using the command:
      ```
      terraform destroy
      ```

      {% note alert %}

      Terraform deletes all the resources that you created in the current configuration, such as clusters, networks, subnets, and VMs.

      {% endnote %}

   1. Confirm the deletion of resources.

- Yandex Cloud Toolkit

   You can delete a function using the [Yandex Cloud Toolkit plugin](https://github.com/yandex-cloud/ide-plugin-jetbrains/blob/master/README.en.md) for the IDE family on the [IntelliJ platform](https://www.jetbrains.com/opensource/idea/) from [JetBrains](https://www.jetbrains.com/).

{% endlist %}
