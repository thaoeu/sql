

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
| date       | timestamp |
| string(id) | varchar   |
| string     | bigint    |
|------------|-----------|
| StrField   | varchar   |
| plong      | bigint    |







ALTER TABLE ori_wechat_solr.wechat_follow_user ADD updatedBy bigint NULL COMMENT '更新用户';

ALTER TABLE ori_wechat_solr.wechat_user_add_external ADD (
createdBy bigint NULL COMMENT '创建用户',
updatedAt timestamp NULL COMMENT '更新时间',
updatedBy bigint NULL COMMENT '更新用户'
)
