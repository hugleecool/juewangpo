juewangpo
=========

An amazing bravo excellent web application written in Python and Flask and Bootstrap, driven in
SAE PaaS.

Deployment
------------
- Use SVN to taken the '1'package to SAE. 
- visit *host/admin/initdb* to init the database.
- visit *host/admin/initusers* to create random users.


##Features
- By detect the os.environ, juewangpo can change mysql server automatically
- Use `SQLAlchemy` and `Flask-SQLAlchemy` to make sql models
- Use `PIL` to convert img then save in SAE Storage
-  `register` `login` `match` `follow` `message`.

##Docs
###`/match`
1. 匹配表，过滤用户当天的匹配次数，转为int类型
2. 次数字典，根据用户角色提供最大次数

        times = int(MatchingRecord.query.filter_by(player=g.user.id,matching_date=date.today()).count())
        max = config.TIMES.get(g.user.role)
        if times >= max:
            flash(u'你今天已匹配%s次，明天再来吧~' % max)
            return render_template('match.html', form=form)
3. 待续

###`models`
1. lala
2. gaga

##WEBsite
[juewangpo.sinaapp.com](http://juewangpo.sinaapp.com)
