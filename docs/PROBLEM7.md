## ๐ ๊ธฐ๋ฅ ์๊ตฌ ์ฌํญ

๋ ๋ฒจ 2์ ํ ํ๋ก์ ํธ ๋ฏธ์์ผ๋ก SNS(Social Networking Service)๋ฅผ ๋ง๋ค๊ณ ์ ํ๋ ํ์ด ์๋ค. ํ์ ์ํ ํฌ๋ฃจ ์ค ํ์ ์๊ณ ๋ฆฌ์ฆ์ ๊ด์ฌ์ด ๋ง์ ๋ฏธ์คํฐ์ฝ๋ ์น๊ตฌ ์ถ์ฒ ์๊ณ ๋ฆฌ์ฆ์ ๊ตฌํํ๊ณ ์ ์๋์ ๊ฐ์ ๊ท์น์ ์ธ์ ๋ค.

- ์ฌ์ฉ์์ ํจ๊ป ์๋ ์น๊ตฌ์ ์ = 10์  
- ์ฌ์ฉ์์ ํ์ ๋ผ์ธ์ ๋ฐฉ๋ฌธํ ํ์ = 1์ 

์ฌ์ฉ์ ์์ด๋ user์ ์น๊ตฌ ๊ด๊ณ ์ ๋ณด friends, ์ฌ์ฉ์ ํ์ ๋ผ์ธ ๋ฐฉ๋ฌธ ๊ธฐ๋ก visitors๊ฐ ๋งค๊ฐ๋ณ์๋ก ์ฃผ์ด์ง ๋, ๋ฏธ์คํฐ์ฝ์ ์น๊ตฌ ์ถ์ฒ ๊ท์น์ ๋ฐ๋ผ ์ ์๊ฐ ๊ฐ์ฅ ๋์ ์์ผ๋ก ์ ๋ ฌํ์ฌ ์ต๋ 5๋ช์ return ํ๋๋ก solution ๋ฉ์๋๋ฅผ ์์ฑํ๋ผ. ์ด๋ ์ถ์ฒ ์ ์๊ฐ 0์ ์ธ ๊ฒฝ์ฐ ์ถ์ฒํ์ง ์์ผ๋ฉฐ, ์ถ์ฒ ์ ์๊ฐ ๊ฐ์ ๊ฒฝ์ฐ๋ ์ด๋ฆ์์ผ๋ก ์ ๋ ฌํ๋ค.

### ์ ํ์ฌํญ

- user๋ ๊ธธ์ด๊ฐ 1 ์ด์ 30 ์ดํ์ธ ๋ฌธ์์ด์ด๋ค.
- friends๋ ๊ธธ์ด๊ฐ 1 ์ด์ 10,000 ์ดํ์ธ ๋ฆฌ์คํธ/๋ฐฐ์ด์ด๋ค.
- friends์ ๊ฐ ์์๋ ๊ธธ์ด๊ฐ 2์ธ ๋ฆฌ์คํธ/๋ฐฐ์ด๋ก [์์ด๋ A, ์์ด๋ B] ์์ผ๋ก ๋ค์ด์๋ค.
  - A์ B๋ ์น๊ตฌ๋ผ๋ ์๋ฏธ์ด๋ค.
  - ์์ด๋๋ ๊ธธ์ด๊ฐ 1 ์ด์ 30 ์ดํ์ธ ๋ฌธ์์ด์ด๋ค.
- visitors๋ ๊ธธ์ด๊ฐ 0 ์ด์ 10,000 ์ดํ์ธ ๋ฆฌ์คํธ/๋ฐฐ์ด์ด๋ค.
- ์ฌ์ฉ์ ์์ด๋๋ ์ํ๋ฒณ ์๋ฌธ์๋ก๋ง ์ด๋ฃจ์ด์ ธ ์๋ค.
- ๋์ผํ ์น๊ตฌ ๊ด๊ณ๊ฐ ์ค๋ณตํด์ ์ฃผ์ด์ง์ง ์๋๋ค.
- ์ถ์ฒํ  ์น๊ตฌ๊ฐ ์๋ ๊ฒฝ์ฐ๋ ์ฃผ์ด์ง์ง ์๋๋ค.

### ์คํ ๊ฒฐ๊ณผ ์์

| user | friends | visitors | result |
| --- | --- | --- | --- |
| "mrko" | [ ["donut", "andole"], ["donut", "jun"], ["donut", "mrko"], ["shakevan", "andole"], ["shakevan", "jun"], ["shakevan", "mrko"] ] | ["bedi", "bedi", "donut", "bedi", "shakevan"] | ["andole", "jun", "bedi"] |

## PROBLEM7 ๊ธฐ๋ฅ ๊ตฌํ ์ฌํญ
    ๋ต์ ์ ๋ ฌ ๊ธฐ์ค 
      (1)์ ์ ๋ด๋ฆผ์ฐจ์ - ์ ์ ๊ฐ์ผ๋ฉด -> (2)์ด๋ฆ ์ค๋ฆ์ฐจ์ ์ผ๋ก ์ต๋ 5๋ช
    
    ๊ตฌํ
    - myFriends ๋ฐฐ์ด ์์ฑ, ์ ์์ ์ฅ HashMap ์์ฑ
    - ๋ฐ๋ณต๋ฌธ์ ํตํด friends๋ฐฐ์ด ๋ด๋ถ์์ friends[1]์ด user์ธ friends[0] myFriends์ ์ ์ฅ
    - ์ ์ ์ถ๊ฐ 
      - ํจ๊ป ์๋ ์น๊ตฌ ์ ์ ์ ์ ์ถ๊ฐ
      - ํ๋กํ ๋ฐฉ๋ฌธ ์ ์ ์ถ๊ฐ : ์ด๋ฏธ ์น๊ตฌ์ธ ์ฌ๋์ ์ถ๊ฐX
    - ์ ์ ์ ์ฅ HashMap์ ์ ์ ์ ์ฅ List๋ก ๋ณํ
    - ์ ์ ์ ์ฅ List๋ฅผ ๊ธฐ์ค๋๋ก ์ ๋ ฌ ํ ์ต๋ 5๊ฐ ๋ฐํ