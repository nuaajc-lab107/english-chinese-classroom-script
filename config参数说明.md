```json
{
    "setting":{
        "emailInform":{//邮箱通知设置
            "sw": 0,//0代表关，1代表开
            "smtpHost": "", //SMTP服务器地址
            "smtpPort": "", //SMTP服务器端口
            "email":"", //发送方邮箱
            "password":"" //邮箱授权码或App密码
        },
        "aiSetting": {
            "aiType": "CHATGLM",//目前只支持智普清言的AI，智普填CHATGLM就行
            "API_KEY": "",//AI的API_KEY自己去智普清言官网获取（有免费余额的）
        }
    },
    "users": [
        {
            "accountType": "CANGHUI",//指定平台，"YINGHUA"代表英华学堂（创能平台也使用这个），CANGHUI代表仓辉平台，ENAEA代表学习公社
            "url": "url",//学习公社不用配，其他平台必须配平台主页的根url，不同学校url不同，比如https://mooc.xxx.cn/，注意千万别带uri指别写成https://mooc.xxx.cn/xxx/xxx这样。
            "account": "账号",//账号
            "password": "密码",//密码
            "coursesCustom": {
                "videoModel": 1,//模式设定，0代表不刷视屏，1为普通模式，2为暴力模式，默认为1，暴力模式目前只支持仓辉
                "autoExam": 1,//是否自动考试，0代表不考，1代表考，默认为0，注意，目前自动考试只支持仓辉和英华！！！
                "excludeCourses": ["课程1", "课程2"],//这个参数代表需要排除不刷的课程，复制课程的名称填入即可（一字不差）
                "includeCourses": ["课程3", "课程4"],//这个指的是需要刷的课程，如果不填默认刷全部课程除非设置了排除课程（注意，如果刷的是学习公社，这里是必须要配置的，配置我的学习列表里面对应选项名称就行，比如“必修课程”、“党纪必修课程”）
                "coursesSettings": [
                    {
                        "name": "大学生劳动教育", //对应需要单独需要客制化的课程名称
                        "includeExams": ["试卷名称1","试卷名称2"],//对应课程需要考试的试卷名称
                        "excludeExams": ["试卷名称3","试卷名称4"],//对应课程不需要考试的试卷名称
                    }
                ]
            }
        }
    ]
}
```

