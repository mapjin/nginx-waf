# nginx-waf
基于Openresty或nginx+lua的WAF防火墙
#由于ngx_lua_waf已经是几年前东西了，需要进行大幅度改造

#参考https://github.com/loveshell/ngx_lua_waf

功能点：<br>
--支持IP白名单和黑名单功能，直接将黑名单的IP访问拒绝。<br>
--支持URL白名单，将不需要过滤的URL进行定义。<br>
--支持User-Agent的过滤，匹配自定义规则中的条目，然后进行处理（返回403）。<br>
--支持CC攻击防护，单个URL指定时间的访问次数，超过设定值，直接返回403。<br>
--支持Cookie过滤，匹配自定义规则中的条目，然后进行处理（返回403）。<br>
--支持URL过滤，匹配自定义规则中的条目，如果用户请求的URL包含这些，返回403。<br>
--支持URL参数过滤，原理同上。<br>
--支持日志记录，将所有拒绝的操作，记录到日志中去。<br>
--日志记录为JSON格式，便于日志分析，例如使用ELKStack进行攻击日志收集、存储、搜索和展示。<br>
--对POST和GET的过滤<br>

