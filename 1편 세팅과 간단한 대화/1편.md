[영상 버전도 있어요!](https://youtu.be/o6te3AbTVF4)
# 1 모듈 설치
### 첫번째로는 디스코드 봇 코딩에 필요한 'asyncio', 'discord.py' 라는 모듈을 설치해야합니다.
터미널을 열고 아래 명령어를 입력해줍시다
```
pip install discord
pip install asyncio
```
# 2 기본적인 틀
### 봇을 구동하기 위한 기본적인 틀입니다.
아래 코드를 따라해주세요
```py
import discord # 디스코드 임포트
from discord.ext import commands # 디스코드 임포트 2
import asyncio # asyncio 임포트

bot = commands.Bot(command_prefix="접두사") # 접두사 설정

bot.run("토큰을 넣어주세요") # 봇 구동 코드
```
# 3 봇 토큰구하기
### 아래에 적힌데로 따라해주세요!
1. 먼저 [디스코드 개발자](https://discord.com/developers) 페이지로 이동합니다!

2. 오른쪽 위, New application를 클릭하세요!
<img src="https://github.com/TEAMTEB/discord.py-ext-class/blob/main/1%ED%8E%B8%20%EC%84%B8%ED%8C%85%EA%B3%BC%20%EA%B0%84%EB%8B%A8%ED%95%9C%20%EB%8C%80%ED%99%94/v11.png?raw=true">

3. Name 칸에 봇의 이름을 적어주세요!
<img src="https://github.com/TEAMTEB/discord.py-ext-class/blob/main/1%ED%8E%B8%20%EC%84%B8%ED%8C%85%EA%B3%BC%20%EA%B0%84%EB%8B%A8%ED%95%9C%20%EB%8C%80%ED%99%94/v12.png?raw=true">

4. Create를 클릭해주세요!

5. 옆의 메뉴에서 Bot 클릭 후 Add bot 클릭
<img src="https://github.com/TEAMTEB/discord.py-ext-class/blob/main/1%ED%8E%B8%20%EC%84%B8%ED%8C%85%EA%B3%BC%20%EA%B0%84%EB%8B%A8%ED%95%9C%20%EB%8C%80%ED%99%94/v13.png?raw=true">

6. 확인창에서 Yes! do it!
<img src="https://github.com/TEAMTEB/discord.py-ext-class/blob/main/1%ED%8E%B8%20%EC%84%B8%ED%8C%85%EA%B3%BC%20%EA%B0%84%EB%8B%A8%ED%95%9C%20%EB%8C%80%ED%99%94/v14.png?raw=true">

7. 아래로 조금 내려서 token 밑에 Copy 클릭!
<img src="https://github.com/TEAMTEB/discord.py-ext-class/blob/main/1%ED%8E%B8%20%EC%84%B8%ED%8C%85%EA%B3%BC%20%EA%B0%84%EB%8B%A8%ED%95%9C%20%EB%8C%80%ED%99%94/v15.png?raw=true">

### 토큰 얻기를 성공하셨습니다!
이제 아까 그곳에 붙여넣어줍니다!
# 4 준비 완료 알림 만들기
이번에는 봇 실행이 완료되었을때 준비 완료를 알리는 코드를 만들어보겠습니다!
```py
@bot.event # 봇에게 이벤트가 발생
async def on_ready(): # 준비되었을때
    print(bot.user.name) # 봇의 유저네임 출력
    print("준비 완료!") # '준비 완료!' 출력!
```
위 코드를 따라해주세요!

코드 설명은 옆에 있으니 필요 없겠죠?
# 5 간단한 명령어
테스트라고 말하면 ㅎㅇㅎㅇ라고 전송하는 코드를 만들어보겠습니다!

메시지를 보내는 코드는 아래와 같습니다!
```py
await (채널형 변수).send("메시지(변수도 가능)")
```
그렇다면 바로 만들어보겠습니다!

먼저 맨 위에 이 코드를 넣어줍니다
```py
@bot.command(name="테스트")
```
이 코드는 '테스트' 커맨드가 입력되었을때 실행된다~ 이런 뜻입니다!

* 참고! 커맨드를 입력할때는 앞에 접두사가 붙어야해요! 아니라면 괜히 한거겠죠?

그 다음으로는 아래 코드를 넣어줍니다
```py
async def test(ctx):
```
여러분이 보낸 메시지를 ctx라고 지정하네요~ 어디보자... 그 다음줄은?!
```py
    await ctx.send("ㅎㅇㅎㅇ")
```
드디어 나왔네요! 대망의 send!

* 참고! 앞의 await은 **꼭 너무나도 진짜진짜 레알**로 중요합니다! 꼭 기억해주세요!
# 6 대망의 실행...
실행을 해보겠습니다!
두구두구두구 과연?!

.

.

.

.

.

.

<img src="https://github.com/TEAMTEB/discord.py-ext-class/blob/main/1%ED%8E%B8%20%EC%84%B8%ED%8C%85%EA%B3%BC%20%EA%B0%84%EB%8B%A8%ED%95%9C%20%EB%8C%80%ED%99%94/v16.png?raw=true">

### 성공하였습니다!!!
유익하셨다면 많은 공유 부탁드려요!

# 다음 영상 관련...

다음 영상은 어떤분의 영상에 따라 **임베드 사용**에 대해 살펴볼 예정입니다!

많은 기대 부탁드려요~!

[영상 버전도 있어요!](https://youtu.be/o6te3AbTVF4)

ⓒ2020 팀 텝
