```flow
    st=>start: 开始
    op1=>operation: 云端系统实时检测作业人员和车辆及现场垃圾信息
    cond1=>condition: 云端系统创建并派发作业任务
    sub1=>subroutine: 作业人员/车辆接收任务并前往指定地点
    cond2=>condition: 判断作业场景是否简单
    op2_1=>operation: 环卫车辆自主作业（简单场景）
    op2_2=>operation: 环卫工人与车辆协同作业（复杂场景）
    mon=>operation: 云端系统持续监控作业进度和效果
    adj=>operation: 根据需要调整作业计划
    warn=>operation: 预警和报警功能（如需要）
    check=>operation: 现场管理人员验收作业结果
    report=>operation: 管理人员上报作业结果至云平台
    end=>end: 结束

    st->op1->cond1
    cond1->sub1
    sub1->cond2
    cond2(yes)->op2_1->mon
    cond2(no)->op2_2->mon
    mon->adj
    adj->warn(right)->mon
    mon->check
    check->report
    report->end
    ```
    ```markdown

上述代码是一个基于Markdown格式的流程图描述，您可以使用支持Markdown格式的流程图工具（如Mermaid等）来渲染这个流程图。在渲染后的流程图中，各个步骤和条件判断将清晰地展示智慧环卫人机协同系统的相关流程。
