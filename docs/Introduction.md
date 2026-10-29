## RobotAgent


(KOR)

- Robot Agent는 AI Agent를 사용해봤는데, 반복적인 작업을 할때마다, 기존에 수행했던 방식을 SKILLS 파일을 읽고 반복합니다, 하지만 단기간에 웹페이지의 UI가 바뀌지 않기에
RobotFramework와 Asciinema 사용해서 Skills 파일이 아닌 robot 파일을 기반으로 작동하며 스크린샷,동영상 녹화,터미널 기록등으로 전체 과정을 기록하고 Agent가 일일이 자동화 루프를 만들고
하면 좋겠지만 돈이 너무 많이 드는 문제가 있어서 일단 정말 자주하는 반복은 인간이 만들어주면 AI Agent가 Crontab 등으로 실행된 결과를 보고  자기가 코드를 수정해주면 좋을듯 해서 만들었습니다.
- AI Agent용 디버깅 툴이자 토큰 절약형 Agent를 만들고 싶습니다. (자료 취합이나 버튼을 누르는 동작을 사람이 하면서 기록하고, AI Agent가 실행결과 읽고 OCR로 데이터 추출해서 기록하면, 약간의
  결과를 읽기 위한 토큰만 쓰기에 Agent를 더 싸고 오래, 그리고 AI API 가격등이 폭등하거나 오픈 모델 날아가면 로컬 llm으로도 감당할 수 있는 루프를 쉽게 만들기 위해 이런 프로젝트를 만들게 되었습니다.)
  - 아직은 구상단계이지만 더 좋은 아이디어 있으면 이슈로 남겨주세요 ^v^

 (ENG)
(LLM Translation)
- Robot Agent: I've tried using AI Agents, but for repetitive tasks, they read the SKILLS files and repeat previous workflows every time. However, since webpage UIs don't change in the short term, it would be better to operate based on .robot files instead of SKILLS files, using Robot Framework and Asciinema to record the entire process via screenshots, video recordings, and terminal logs. While it would be nice for the Agent to build automation loops step-by-step, it costs way too much money. Therefore, I built this because it would be great if humans create the scripts for frequently repeated tasks, andthen an AI Agent—triggered by Crontab or similar schedulers—simply reviews the execution results and modifies the code itself.
I want to build a debugging tool for AI Agents and a token-efficient Agent. (By having humans perform actions like data gathering or clicking buttons while recording, and then having the AI Agent read the execution results and extract data via OCR to log them, it only consumes a minimal amount of tokens just to read the results. This makes the Agent cheaper and longer-lasting, and easily creates a loop that can be handled even by local LLMs if AI API prices spike or open-source models disappear.)
This is still in the conceptual stage, so feel free to leave feedback or better ideas as issues ^v^
