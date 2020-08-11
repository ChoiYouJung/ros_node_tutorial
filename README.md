# ros_node_tutorial
ROS_Foundation_Programming

Topic1. Publisher-Subscriber

	$ roscore

	$ rosrun ros_node_tutorial topic_publisher

	$ rosrun ros_node_tutorial topic_subscriber

Topic2. Service server-Service client

	$ roscore

	$ rosrun ros_node_tutorial service_server

	$ rosrun ros_node_tutorial service_client number1(type:int64) number2(type:int64) 
	
	(example : $ rosrun ros_node_tutorial action_client 3 2)

Topic3. Action server-Action client

	$ roscore

	$ rosrun ros_node_tutorial action_server

	$ rosrun ros_node_tutorial action_client
	

Topic4. Parameter(example:Service node)

	$ roscore
	
	$ rosrun ros_node_tutorial action_param_server
	
	<parameter setting & service execution>
	
		1) parameter setting 
			
			$ rosparam set /calculation_method number
			* number range(1(+),2(-),3(*),4(/))
			
		2) service execution
			
			$ rosparam call /ros_tutorial_srv number1(type:int64) number2(type:int64)
			
			(example : $ rosparam call /ros_tutorial_srv 10 5)

Topic5. roslaunch

	case 1:
		
		$ roscore
	
		$ roslaunch ros_tutorial_topic union.launch --screen
		
		$ rqt_graph
		
	case 2:
	
		$ roscore
		
		$ roslaunch ros_tutorial_topic union_2.launch --screen
		
		$ rqt_graph
