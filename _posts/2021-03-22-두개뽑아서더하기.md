---
layout: post
title: "프로그래머스"
date: 2020-03-22
excerpt: "두 개 뽑아서 더하기"
tags: [java, programmers, test, study, everyday]
comments: true
---

## 문제 

정수 배열 numbers가 주어집니다.

numbers에서 서로 다른 인덱스에 있는 두 개의 수를 뽑아 더해서 만들 수 있는 모든 수를 배열에 오름차순으로 담아 return 하도록 solution 함수를 완성해주세요.
 
제한사항
numbers의 길이는 2 이상 100 이하입니다.
numbers의 모든 수는 0 이상 100 이하입니다.

---

## 풀이

* ArrayList 사용


```
class Solution {
    public int[] solution(int[] numbers) {
        ArrayList<Integer> list = new ArrayList<Integer>();
        
        for(int i=0; i<numbers.length; i++){
            for(int j=i+1;j<numbers.length; j++){
                int a = numbers[i]+numbers[j];
                if (list.indexOf(a) < 0){
                	list.add(a);
                }
            }
        }
        int[] answer = new int[list.size()];
        for (int i = 0; i < list.size(); i++) {
            answer[i] = list.get(i);
        }
        Arrays.sort(answer);

        return answer;
    }
}

```


## 애로사항
* 중복값을 어떻게 제거할 것인가


## 해결방법
* ArrayList의 indexOf메소드를 사용하여 해결
* 블로그를 참고하여 indexOf 를 알아보았다

## 요약
* indexOf(Object) Object 값이 있으면 있는 해당배열의 번호를 리턴, 없으면 -1을 리턴한다.

## 참고
* HashSet을 이용한 방법도 있다

```
import java.util.HashSet;
import java.util.Set;

class Solution {
     public int[] solution(int[] numbers) {
        Set<Integer> set = new HashSet<>();

        for(int i=0; i<numbers.length; i++) {
            for(int j=i+1; j<numbers.length; j++) {
                set.add(numbers[i] + numbers[j]);
            }
        }

        return set.stream().sorted().mapToInt(Integer::intValue).toArray();
    }
}
```

* HashSet 특징 : 중복이 허용되지 않는다, 순서를 보장 하지 않는다 , null 값을 저장할 수 있다, 내부적으로 HashMap을 사용하여 데이터를 저장한다.
