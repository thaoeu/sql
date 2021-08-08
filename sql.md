CREATE TABLE ori_wechat_solr.wechat_corp_tag (
id varchar(10) NOT NULL COMMENT 'id'
)
ENGINE=InnoDB
DEFAULT CHARSET=utf8mb4
COLLATE=utf8mb4_unicode_ci
COMMENT='企业微信客户标签表';

ALTER TABLE ori_wechat_solr.wechat_corp_tag ADD (
name bigint NULL COMMENT '标签名称',
group_id bigint NULL COMMENT '所属标签组id',
createtime bigint NULL COMMENT '标签创建时间'
)




CREATE TABLE ori_wechat_solr.wechat_corp_tag_group (
id varchar(10) NOT NULL COMMENT 'id',
group_id bigint NULL COMMENT '标签组id', 
group_name bigint NULL COMMENT '标签组名称', 
createtime plong NULL COMMENT '标签组创建时间', 
order tinyint NULL COMMENT '标签组排序的次序值', 
deleted bit NULL COMMENT '是否被删除', 
taglist bigint NULL COMMENT '标签id列表', 
type tinyint NULL COMMENT '类型', 
dataDate timestamp NULL COMMENT '数据时间', 
createdAt timestamp NULL COMMENT '创建时间', 
createdBy bigint NULL COMMENT '创建用户', 
updatedAt timestamp NULL COMMENT '更新时间', 
updatedBy bigint NULL COMMENT '更新用户', 
)
ENGINE=InnoDB
DEFAULT CHARSET=utf8mb4
COLLATE=utf8mb4_unicode_ci
COMMENT='企业微信客户标签组表';

CREATE TABLE ori_wechat_solr.wechat_external_contact_remark (
 id varchar(100) NOT NULL COMMENT 'id',
 userid bigint NULL COMMENT '员工id',
 external_userid bigint NULL COMMENT '客户id',
 remark bigint NULL COMMENT '备注',
 remark_corp_name bigint NULL COMMENT '客户的企业名称',
 remark_mobiles bigint NULL COMMENT '客户手机',
 remark_pic_mediaid bigint NULL COMMENT '备注图片id',
 description bigint NULL COMMENT '描述'
)
ENGINE=InnoDB
DEFAULT CHARSET=utf8mb4
COLLATE=utf8mb4_unicode_ci
COMMENT='企业微信员工对客户备注表';

-----
全手动
-----

CREATE TABLE ori_wechat_solr.wechat_external_contact_remark (
id varchar NOT NULL COMMENT '表id',
userid bigint NULL COMMENT '员工id',
external_userid bigint NULL COMMENT '客户id',
remark bigint NULL COMMENT '备注',
remark_corp_name bigint NULL COMMENT '客户的企业名称',
remark_mobiles bigint NULL COMMENT '客户手机',
remark_pic_mediaid bigint NULL COMMENT '备注图片id',
description bigint NULL COMMENT '描述',
createtime bigint NULL COMMENT '添加时间',
state bigint NULL COMMENT '添加渠道',
taglist bigint NULL COMMENT '标签',
tag bigint NULL COMMENT '标签',
`tags.group_name` bigint NULL COMMENT '标签分组名',
`tags.tag_name` bigint NULL COMMENT '标签名',
`tags.tag_name` bigint NULL COMMENT '标签名'
`tags.type` pint NULL COMMENT '标签类型',
remarkid bigint NULL COMMENT '备注id',
dataDate timestamp NULL COMMENT '数据时间',
status int NULL COMMENT '状态',
createdAt timestamp NULL COMMENT '创建时间',
createdBy bigint NULL COMMENT '创建用户',
updatedAt timestamp NULL COMMENT '更新时间',
updatedBy bigint NULL COMMENT '更新用户'
)
ENGINE=InnoDB
DEFAULT CHARSET=utf8mb4
COLLATE=utf8mb4_unicode_ci
COMMENT='企业微信员工对客户备注表';

CREATE TABLE ori_wechat_solr.wechat_external_contact_remark (
 id varchar(100) NOT NULL COMMENT 'id',
 userid bigint NULL COMMENT '员工id',
 external_userid bigint NULL COMMENT '客户id',
 remark bigint NULL COMMENT '备注',
 remark_corp_name bigint NULL COMMENT '客户的企业名称',
 remark_mobiles bigint NULL COMMENT '客户手机',
 remark_pic_mediaid bigint NULL COMMENT '备注图片id',
 description bigint NULL COMMENT '描述'
)
ENGINE=InnoDB
DEFAULT CHARSET=utf8mb4
COLLATE=utf8mb4_unicode_ci
COMMENT='企业微信员工对客户备注表';





CREATE TABLE ori_wechat_solr.wechat_external_contact_remark (
id varchar NOT NULL COMMENT '表id',
userid bigint NULL COMMENT '员工id',
external_userid bigint NULL COMMENT '客户id',
remark bigint NULL COMMENT '备注',
remark_corp_name bigint NULL COMMENT '客户的企业名称',
remark_mobiles bigint NULL COMMENT '客户手机',
remark_pic_mediaid bigint NULL COMMENT '备注图片id',
description bigint NULL COMMENT '描述',
createtime long NULL COMMENT '添加时间',
state bigint NULL COMMENT '添加渠道',
taglist bigint NULL COMMENT '标签',
tag bigint NULL COMMENT '标签',
`tags.group_name` bigint NULL COMMENT '标签分组名',
`tags.tag_name` bigint NULL COMMENT '标签名',
`tags.type` pint NULL COMMENT '标签类型',
remarkid bigint NULL COMMENT '备注id',
dataDate timestamp NULL COMMENT '数据时间',
status int NULL COMMENT '状态',
createdAt timestamp NULL COMMENT '创建时间',
createdBy bigint NULL COMMENT '创建用户',
updatedAt timestamp NULL COMMENT '更新时间',
updatedBy bigint NULL COMMENT '更新用户'
)
ENGINE=InnoDB
DEFAULT CHARSET=utf8mb4
COLLATE=utf8mb4_unicode_ci
COMMENT='企业微信员工对客户备注表';

CREATE TABLE ori_wechat_solr.wechat_external_contact (
 id varchar(10) NOT NULL COMMENT '表id',
external_userid bigint NULL COMMENT '外部人id',
name bigint NULL COMMENT '外部联系人名称',
avatar bigint NULL COMMENT '头像',
type int NULL COMMENT '类型',
gender int NULL COMMENT '性别',
unionid bigint NULL COMMENT '微信身份标识',
position bigint NULL COMMENT '职位',
corp_name bigint NULL COMMENT '企业名简称',
corp_full_name bigint NULL COMMENT '企业名全称',
external_profile bigint NULL COMMENT '扩展信息',
createdAt timestamp NULL COMMENT '创建时间',
createdBy bigint NULL COMMENT '创建用户',
updatedAt timestamp NULL COMMENT '更新时间',
updatedBy bigint NULL COMMENT '更新用户'
)
ENGINE=InnoDB
DEFAULT CHARSET=utf8mb4
COLLATE=utf8mb4_unicode_ci
COMMENT='企业微信客户表';

转换表
| solr       | mysql     |
|------------|-----------|
| int        | int       |
| timestamp       | timestamp |
| string(id) | varchar   |
| bigint     | bigint    |
|------------|-----------|
| StrField   | varchar   |
| plong      | bigint    |





tinyint


ALTER TABLE ori_wechat_solr.wechat_follow_user ADD updatedBy bigint NULL COMMENT '更新用户';

ALTER TABLE ori_wechat_solr.wechat_user_add_external ADD (

`tags.group_name` bigint NULL COMMENT '标签分组名',
`tags.tag_name` bigint NULL COMMENT '标签名',
`tags.tag_name` bigint NULL COMMENT '标签名'
`tags.type` pint NULL COMMENT '标签类型',
createdBy bigint NULL COMMENT '创建用户',
updatedAt timestamp NULL COMMENT '更新时间',
updatedBy bigint NULL COMMENT '更新用户'
)


ALTER TABLE ori_wechat_solr.wechat_external_contact_remark ADD taglist bigint NULL COMMENT '标签';

ALTER TABLE ori_wechat_solr.wechat_external_contact_remark ADD (
`tags.tag_name` bigint NULL COMMENT '标签名',
`tags.type` pint NULL COMMENT '标签类型'
)
