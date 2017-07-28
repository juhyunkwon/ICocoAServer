#######################################################################
##### ICocoAServer - 현재
####################### 모바일 서버 아키텍처 ############################

a. native-server [ tcp / udp ]
- iocp &  [ socket handler ]
- FlatBuffers [ serialization ]
- hiredis [ session verification ]
- jsoncpp [ web-front request ]
- log4c [ logger handler ]

b. client interface
- SuperSocket c# ( tcp )
- LiteNetLib c# ( udp )
- FlatBuffers [ serialization ]

c. web-front
- php7 ( slimFramework 3.x ), php-fpm, nginx
	+ packet manager ( session, encrypt )
	+ url validation ( packet )
	+ update game share data
- log4php [ logger handler ]

d. rdbms & cache
- redis, mariadb, mongodb

e. features
- service ( background daemon manager )
- logic ( contents manager )
- logger ( log manager )
- core ( network event manager, thread pool )
- link ( server to server manager )



#######################################################################
##### ICocoAServer - 업그레이드
####################### 모바일 서버 아키텍처 ############################

a. native-server [ tcp / udp ]
- Boost.Asio [ socket handler ]


#######################################################################
##### ICocoAServer - 이후
####################### 모바일 서버 아키텍처 ############################

a. zeroMQ 를 이용한 모바일 게임 서버 설계
