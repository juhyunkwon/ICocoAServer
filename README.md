#######################################################################
##### ICocoAServer [  ]
####################### 모바일 서버 아키텍처 ############################





#######################################################################
##### ICocoAServer [  ]
####################### 모바일 서버 아키텍처 ############################
a. native-server [ tcp / udp ]
- Boost.Asio [ socket handler ]
- FlatBuffers [ serialization ]
- hiredis [ session verification ]
- jsoncpp [ web-front request ]
- log4c [ logger handler ]

b. client interface
- SuperSocket c# ( tcp )
- LiteNetLib c# ( udp )
- FlatBuffers [ serialization ]

c. web-front
- php7 (PSR4), php-fpm, nginx
- log4php [ logger handler ]

d. rdbms & cache
- redis, mariadb, mongodb

e. features
- service ( background daemon manager )
- logic ( contents manager )
- logger ( log manager )
- core ( network event manager, thread pool )
- link ( server to server manager )

e. 생각해 보고 있는 문제?
- 서버 엔진 코어 구조
- 분산 환경 구조
- 압축 및 알고리즘 관련
- AWS 서비스 구조
