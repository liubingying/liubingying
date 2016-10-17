生成的数据ER图
![image]
(http://github.com/liubingying/liubingying/raw/master/D:\liubingying\liubingying/ERtu.png


sql语句
DROP TABLE IF EXISTS `device_cost`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!40101 SET character_set_client = utf8 */;
CREATE TABLE `device_cost` (
  `device_cost_id` int(11) NOT NULL,
  `device_id` int(11) NOT NULL,
  `devicefix_date` datetime NOT NULL,
  `device_cost_stuff` varchar(200) NOT NULL,
  PRIMARY KEY (`device_cost_id`),
  KEY `device_id_idx` (`device_id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `device_cost`
--

LOCK TABLES `device_cost` WRITE;
/*!40000 ALTER TABLE `device_cost` DISABLE KEYS */;
INSERT INTO `device_cost` VALUES (1,1,'2016-10-10 00:00:00','接线盒'),(2,2,'2016-10-10 00:00:00','控制箱'),(3,3,'2016-10-10 00:00:00','悬架'),(4,4,'2016-10-10 00:00:00','气泵');
/*!40000 ALTER TABLE `device_cost` ENABLE KEYS */;
UNLOCK TABLES;



DROP TABLE IF EXISTS `devicefix_info`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!40101 SET character_set_client = utf8 */;
CREATE TABLE `devicefix_info` (
  `devicefix_id` int(11) NOT NULL,
  `device_id` int(11) NOT NULL,
  `devicefix_date` datetime NOT NULL,
  `devicefix_reason` varchar(200) NOT NULL,
  `devicefix_backdate` datetime NOT NULL,
  `user_id` int(11) NOT NULL,
  PRIMARY KEY (`devicefix_id`),
  KEY `device_id_idx` (`device_id`),
  KEY `user_id_idx` (`user_id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `devicefix_info`
--

LOCK TABLES `devicefix_info` WRITE;
/*!40000 ALTER TABLE `devicefix_info` DISABLE KEYS */;
INSERT INTO `devicefix_info` VALUES (1,1,'2016-10-10 00:00:00','接线盒内卫生清洁；检查进线口密封情况；','2016-10-11 00:00:00',0),(2,2,'2016-10-10 00:00:00','除铁器控制箱内除尘；除铁器线路有无破裂，磨损；','2016-10-11 00:00:00',0),(3,3,'2016-10-10 00:00:00','检查皮带秤速度传感器是否正常；清理皮带秤悬架上杂物；','2016-10-11 00:00:00',0),(4,4,'2016-10-10 00:00:00','检查电缆电缆头固定情况；检查各部位限位开关是否灵活；','2016-10-11 00:00:00',0);
/*!40000 ALTER TABLE `devicefix_info` ENABLE KEYS */;
UNLOCK TABLES;



DROP TABLE IF EXISTS `device_info`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!40101 SET character_set_client = utf8 */;
CREATE TABLE `device_info` (
  `device_id` int(11) NOT NULL,
  `device_name` varchar(45) NOT NULL,
  PRIMARY KEY (`device_id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `device_info`
--

LOCK TABLES `device_info` WRITE;
/*!40000 ALTER TABLE `device_info` DISABLE KEYS */;
INSERT INTO `device_info` VALUES (1,'6000V及以上电机'),(2,'除铁器'),(3,'皮带秤'),(4,'采样机');
/*!40000 ALTER TABLE `device_info` ENABLE KEYS */;
UNLOCK TABLES;
![image]
(http://github.com/liubingying/liubingying/raw/master/D:\liubingying\liubingying/chaxun.png
![image]
(http://github.com/liubingying/liubingying/raw/master/D:\liubingying\liubingying/chaxun2.png


