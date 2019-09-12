* 카카오 오픈채팅
```python
def solution(record):
    answer = []
    chatName={}
    for i in record:
        if i[0].split()[0] == 'E' or i[0].split()[0] == 'C':
            chatName[i.split()[1]] = i.split()[2]
    for i in record:        
        if i[0].split()[0] == 'E': #or i[0].split()[0] == 'C':    
            answer.append(chatName[i.split()[1]]+ '님이 들어왔습니다.')
        elif i[0].split()[0] == 'L':
            answer.append(chatName[i.split()[1]]+ '님이 나갔습니다.')
    return answer
```

record	
["Enter uid1234 Muzi", "Enter uid4567 Prodo","Leave uid1234","Enter uid1234 Prodo","Change uid4567 Ryan"]	

result
["Prodo님이 들어왔습니다.", "Ryan님이 들어왔습니다.", "Prodo님이 나갔습니다.", "Prodo님이 들어왔습니다."]
