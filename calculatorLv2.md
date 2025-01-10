package com.example;

import java.util.LinkedList;
import java.util.Queue;
import java.util.Scanner;

public class Calculator {
    private Queue<String> history = new LinkedList<>();

    public int calculate(int num1, int num2, char operator){

            int result = 0;
            switch (operator) {
                case '+':
                    result = num1 + num2;
                    break;
                case '-':
                    result = num1 - num2;
                    break;
                case '/':
                    if (num2 == 0)
                        System.out.println("나눗셈 연산에서 분모(두번째 정수)에 0이 입력될 수 없습니다.");
                    else
                        result = num1 / num2;
                    break;
                case '*':
                    result = num1 * num2;
                    break;
                default:
                    System.out.println("잘못된 연산자입니다.");
                    return result;
        }

        return result;
    }



