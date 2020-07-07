# Driving Behavior Analysis System

The location cloud driving behavior analysis system is a system to analysis commercial vehicle drivers’ driving behavior, It statistics the trip mileage, fuel, duration, braking time, fatigue driving, engine rotation range, speed range, etc, about 200 indicators.

Responsibility:
First it collects real-time location message(including gps time,speed,latitude,longitude,braking flag,engin e rotation,etc) uploaded by commercial vehicle-mounted terminals,one message per second.
Second ,it executes algorithm chains to calculate trip data(include trip start time ,end time,mileage,fuel,d uration,braking frequency,rapidly accelerate,etc) and event data(ignite event, flameout event, sharp acc eleration event, sharp step on accelerator event,etc).It included real-time statistics(based on Jstrom, co nsumes message on Kafka, then use flume to store trip and event data in Mongo and HBase) and offlin e statistics(use spark, consumes data from the Hive, then store data in the Hive and Mongo).
Third, it gives the trip a score, evaluates the driver's driving behavior and gives hints about what's good and what needs improvement.
Last but not least, it summarizes the trip data to the daily, weekly, monthly reports, and sends a monthly
report to every driver every month.Involving technology including driving behavior algorithm design, Kaf ka, flow calculation, Mongo, Jstrom, Hadoop, Spark and so on


驾驶行为分析系统主要实现对商用车载终端上传的实时位置数据(交通部制定的808协议）收集，过滤、驾驶行为指标计算，最终生成司机的驾驶行为事件和行程数据，并对司机的驾驶行为进行分析，打分和建议。
系统支持200 多个指标的计算，支持实时与离线计算，为下游系统提供数据。
系统涉及实时海量报文数据接入、流计算分布式处理、大数据实时落盘，基础信息 ETL同步等。
目前线上支持 30 万终端设备同时在线。
涉及技术 包括 流计算，大数据，微服务等。
 1.与产品经理对接，确定开发计划，组织及代码评审等工作 2.技术预研及急难问题解决，系统核心代码的开发 及维护，相关的架构设计，性能优化 3.保障系统日常稳定运行，并完成流程梳理、功能设计、文档撰写、流程 搭建 4.需求分析，架构设计，算法设计，代码实现,数据准确性验证。