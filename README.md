# SCSS를 이용한 리팩토링
리팩토링이란?

결과의 변경 없이 코드의 구조를 재조정하는 것

## 사용된 SCSS 기능
- SCSS 중첩 : 선택자 중괄호 안에 바로 하위 선택자를 집어넣어 반복입력을 줄이는 것
- &를 사용하여 상위 선택자 참조
- 반복문 : 값을 집어넣을땐 보간법 (#{$i})사용
```scss
@for $i from 1 through 32 {
                &:nth-child(#{$i}) .image {
                    background-image: url("./images/hero#{$i}.png");
                }
            }
```