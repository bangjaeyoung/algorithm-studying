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
            print (m_count)




