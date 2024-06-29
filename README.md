# Docker Nexus Maven

端口
------
<pre>
8081
</pre>

登录
------
<pre>
http://ip:8081

Username: admin

Password: ./data/admin.password
</pre>

仓库配置
------
<pre>
&lt;repositories&gt;
    &lt;repository&gt;
        &lt;id&gt;maven-public&lt;/id&gt;
        &lt;name&gt;maven-public&lt;/name&gt;
        &lt;url&gt;http://ip:8081/repository/maven-public/&lt;/url&gt;
        &lt;snapshots&gt;
            &lt;enabled&gt;true&lt;/enabled&gt;
        &lt;/snapshots&gt;
        &lt;releases&gt;
            &lt;enabled&gt;true&lt;/enabled&gt;
        &lt;/releases&gt;
    &lt;/repository&gt;
&lt;/repositories&gt;
</pre>

插件仓库
------
<pre>
    &lt;pluginRepositories&gt;
        &lt;pluginRepository&gt;
            &lt;id&gt;maven-plugin-public&lt;/id&gt;
            &lt;name&gt;maven-plugin-public&lt;/name&gt;
            &lt;url&gt;http://ip:8081/repository/maven-public/&lt;/url&gt;
            &lt;releases&gt;
                &lt;enabled&gt;true&lt;/enabled&gt;
            &lt;/releases&gt;
            &lt;snapshots&gt;
                &lt;enabled&gt;false&lt;/enabled&gt;
            &lt;/snapshots&gt;
        &lt;/pluginRepository&gt;
    &lt;/pluginRepositories&gt;
</pre>

发布配置
------
<pre>
&lt;distributionManagement&gt;
    &lt;repository&gt;
        &lt;id&gt;maven-releases&lt;/id&gt;
        &lt;name&gt;maven-releases&lt;/name&gt;
        &lt;url&gt;http://ip:8081/repository/maven-releases/&lt;/url&gt;
    &lt;/repository&gt;
    &lt;snapshotRepository&gt;
        &lt;id&gt;maven-snapshots&lt;/id&gt;
        &lt;name&gt;maven-snapshots&lt;/name&gt;
        &lt;url&gt;http://ip:8081/repository/maven-snapshots/&lt;/url&gt;
    &lt;/snapshotRepository&gt;
&lt;/distributionManagement&gt;
</pre>