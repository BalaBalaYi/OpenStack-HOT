# 记录一下不太友好但比较常用的CLI命令

### Nova
##### 彻底移除nova-compute
```
# 注意先使用nova service-list查询id，并且确定对应主机的主机聚合已经删除
nova service-delete id
```

### Neutron
##### 创建端口
```
neutron port-create --name r10 --fixed-ip subnet_id=9c4e84bd-2ae6-4e1a-b2c9-48662bb5df33,ip_address=192.168.111.10 --tenant-id 303d69063df34068a1573dbd08dda650 95939b3f-cddf-454c-a07f-0297bdc665c7
```

### Swift
##### 上传对象
```
# backup 是一级container
# fuel/20180403 是二级目录
# test 是当前本地路径待上传的文件
openstack object create backup/fuel/20180403 test
```
##### 删除对象
```
# backup 是一级container
# fuel/20180403 是二级目录
# test 是当前本地路径待上传的文件
openstack object delete backup/fuel/20180403 test
```
