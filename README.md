# Conn‘s Personal Website

## 数据库

### 建表

```sql
CREATE TABLE sort (
    id BIGINT(40) NOT NULL AUTO_INCREMENT,
    name VARCHAR(1024) NOT NULL COMMENT '分类名称',
    article_number TINYINT(10) NOT NULL DEFAULT '0' COMMENT '该分类下文章的数量',
    created_time DATETIME NOT NULL COMMENT '分类创建时间',
    modified_time DATETIME NOT NULL COMMENT '分类修改时间',
    is_effective TINYINT(1) NOT NULL DEFAULT '1' COMMENT '是否有效，默认为1有效，为0无效',
    PRIMARY KEY(id)
) ENGINE=INNODB DEFAULT CHARSET=utf8;
```

```sql
CREATE TABLE article (
    id BIGINT(40) NOT NULL AUTO_INCREMENT COMMENT '主键',
    title VARCHAR(256) NOT NULL DEFAULT '' COMMENT '文章标题',
    summary VARCHAR(1024) NOT NULL DEFAULT '' COMMENT '文章简介，默认100个汉字以内',
    content VARCHAR(20480) NOT NULL DEFAULT '' COMMENT '文件位置',
    is_top TINYINT(1) NOT NULL DEFAULT '0' COMMENT '文章是否置顶，0为否，1为是',
    visit_number INT(10) NOT NULL DEFAULT '0' COMMENT '文章访问量',
    created_time DATETIME NOT NULL COMMENT '创建时间',
    modified_time DATETIME NOT NULL COMMENT '修改时间',
    PRIMARY KEY(id)
) ENGINE=INNODB DEFAULT CHARSET=utf8;
```





