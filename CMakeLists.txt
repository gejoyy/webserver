cmake_minimum_required(VERSION 3.16)
project(webserver)

set(CMAKE_CXX_STANDARD 14)

include_directories(.)
include_directories(CGImysql)
include_directories(http)
include_directories(lock)
include_directories(log)
include_directories(threadpool)
include_directories(timer)

add_executable(webserver
        CGImysql/sign.cpp
        CGImysql/sql_connection_pool.cpp
        CGImysql/sql_connection_pool.h
        http/http_conn.cpp
        http/http_conn.h
        lock/locker.h
        log/block_queue.h
        log/log.cpp
        log/log.h
        test_presure/webbench-1.5/socket.c
        test_presure/webbench-1.5/webbench.c
        threadpool/threadpool.h
        timer/lst_timer.cpp
        timer/lst_timer.h
        config.cpp
        config.h
        main.cpp
        webserver.cpp
        webserver.h)
