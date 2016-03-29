# Don't use zawgyi OR Don't change value to zawgyi #
Yes, you can remove or comment at line 96 to 103 in db\_setup.php

current :

```
if (($type=="string") or ($type=="blob"))
{
//Convert TO String
echo 'Convert Line.... '.$curr_line;
$field_name=mysql_field_name($result_query,$field_count);
mysql_query("update ".mysql_tablename($result, $i) ." set `$field_name` = '". myan_conv($col_value)."' where `$field_name`='$col_value'");

}
```

you should do :


```
/* Don't Change Value
if (($type=="string") or ($type=="blob"))
{
//Convert TO String
echo 'Convert Line.... '.$curr_line;
$field_name=mysql_field_name($result_query,$field_count);
mysql_query("update ".mysql_tablename($result, $i) ." set `$field_name` = '". myan_conv($col_value)."' where `$field_name`='$col_value'");

}

*/
```