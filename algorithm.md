자료구조란?

    . 자료구조, 데이터구조, data structure
    . 대량의 데이터를 효율적으로 관리할 수 있는 데이터 구조를 의미
    . 어떤 데이터 구조를 사용하느냐에 따라 코드의 효율이 달라짐

    ※ 대표적인 자료구조
        배열, 스택, 큐, 링크드 리스트, 해쉬 테이블, 힙 등


알고리즘이란?

    . 알고리즘, Algorithm
    . 어떤 문제를 풀기 위한 절차나 방법


* 어떤 자료구조와 알고리즘을 쓰느냐에 따라 코드 성능이 천차만별



1. 배열 (Array)
    
    . 데이터를 나열하고, 각 데이터를 각자의 인덱스에 대응하도록 구성한 데이터 구조
    . 파이썬에서 리스트 타입이 배열 기능임


    배열의 필요성

        . 같은 종류의 데이터를 효율적으로 관리
        . 같은 종류의 데이터를 순차적으로 저장
        . 장점 : 빠른 접근 가능
            첫 데이터 위치에서 인덱스 번호의 위치로 접근
        . 단점 : 데이터 추가/삭제 어려움
            미리 최대 길이를 지정해야 함


        #python

        1차원 배열 (리스트로 구현)
            data_list = [1, 2, 3, 4, 5]

        2차원 배열 (리스트로 구현)
            data_list = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]


        프로그래밍 예제 (직접 푼 풀이만)

        1.  print (data_list[2][2], data_list[2][1], data_list[2][0])

        2.  m_count = 0
            for data in dataset:
                for index in range(len(data)):
                    if data[index] == 'M':
                        m_count += 1
            print(m_count)



2. 큐 (Queue)

    큐의 구조
    
        . 가장 먼저 넣은 데이터를 가장 먼저 꺼낼 수 있는 데이터 구조
        . FIFO(First-In, First-Out), LILO(Last-In, Last-Out), LIFO(Last-In, First-Out) 등의 형태도 존재함


    알아둘 용어

        . Enqueue : 큐에 데이터를 넣는 기능
        . Dequeue : 큐에서 데이터를 꺼내는 기능


    파이썬 queue 라이브러리 활용해서 큐 자료구조 사용하기

        . Queue() : 가장 일반적인 큐 구조 (FIFO 구조)
        . LifoQueue() : 나중에 입력된 데이터가 가장 먼저 출력되는 구조 (스택과 같은 구조)
        . PriorityQueue() : 데이터에 우선순위를 지정해서, 우선순위대로 데이터를 출력하는 구조

    
        여러 큐 형태 중에 기본적인 Queue()로 큐 만들기
        
            import queue

            data_queue = queue.Queue()
            data_queue.put("ex")
            data_queue.put(1)

            #data_queue.qsize() -> 2
            #data_queue.get() -> 'ex'
            #data_queue.get() -> 1
            #data_qsize() -> 0


        여러 큐 형태 중에 기본적인 Queue()로 큐 만들기
        
            import queue

            data_queue = queue.PriorityQueue()
            data_queue.put((10, "korea"))               #가로 두 개인 이유는 튜플이기 때문
            data_queue.put((5, 1))
            data_queue.put((15, "china"))

            #data_queue.qsize() -> 3
            #data_queue.get() -> (5, 1)
            #data_queue.get() -> (10, 'korea')


    큐가 많이 쓰이는 곳

    . 멀티 태스킹을 위한 프로세스 스케쥴링 방식을 구현하기 위해 많이 사용됨 (중요)


        리스트 변수로 큐를 다루는 enqueue, dequeue 기능 구현 예시

        1. queue_list = list()

        def enqueue(data):
            queue_list.append(data)
        
        def dequeue():
            data = queue_list[0]
            del queue_list[0]
            return data

        for index in range(10):
            enqueue(index)

            #len(queue_list) -> 10
            #dequeue() -> 2