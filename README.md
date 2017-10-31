
## itop FAQ 常见问题列表

## 官方Wiki（不需要翻墙）

https://wiki.openitop.org/
里面有详细的文档介绍

比如，调用api进行二次开放

    https://wiki.openitop.org/doku.php?id=2_3_0:advancedtopics:rest_json&s[]=api

个性定制itop

    https://wiki.openitop.org/doku.php?id=2_3_0:customization:start

更多...

### itop在线中文文档 

    http://itop.doc.hardie.me/

### itop 邮件配置


      /conf/production/config-itop.php 改为（默认为只读，修改为可写，操作完后改只读，210版本后可以直接后台配置）
 
        查找email_transport  修改'email_transport' => 'PHPMail'为： 

	'email_transport' => 'SMTP',

	'email_transport_smtp.host' => 'smtp.qq.com',
	'email_transport_smtp.password' => 'sbmht',

	'email_transport_smtp.username' => '1000@qq.com',

        'forgot_password_from' => '1000@qq.com',

###  触发器模版


     来自 
    itop@xxx.com     

    回复到     

    收件人 

    SELECT Person WHERE id= :this->contactid
 
    SELECT Person JOIN lnkPersonToTeam AS T ON T.person_id = Person.id WHERE T.team_id = :this->manager_group_id

抄送 
    

隐送 
 
    

主题 

    你的iTop 账户信息     

邮件体 

     <pre>$this->first_name$ $this->last_name$你好</pre> 

     <pre>你的iTop账户被创建</pre> 
     <pre>iTop 登录地址：</pre> 
     <pre>http://ip/pages/UI.php</pre> 

     <pre>你的用户名为：$this->login$</pre> 

     <pre>用户密码为:xxx</pre> 

     <pre>请登录后更改密码！本邮件为系统自动邮件，请勿回复，任何问题与建议请联系xxx</pre> 

     <pre>xxx公司iTop</pre> 

### profile 角色用户描述翻译

直接修改表 priv_urp_profiles



### 其他问题，持续增加中...





