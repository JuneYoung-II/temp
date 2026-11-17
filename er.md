##문제 1의 DB
```mermaid
erDiagram
    COMPANY {
        string 회사명 PK
        string 산업분야
        int 희망구직자수
        string 신청기간
        int 초봉
    }
    
    JOB_SEEKER {
        string 주민등록번호 PK
        string 전공분야
        float 대학학점
        int 토익성적
        string 자격증
        int 희망연봉
        string 대학이름 FK
    }
    
    UNIVERSITY {
        string 대학이름 PK
        string 주소
        string 대학설명
        int 취업학생수
    }

    HIRED_RECORD {
        string 주민등록번호 PK, FK
        string 회사명 PK, FK
        string 취업상태
    }

    UNIVERSITY ||--o{ JOB_SEEKER : "출신"
    COMPANY ||--o{ APPLY : "지원받음"
    JOB_SEEKER ||--o{ APPLY : "지원함"
    
    JOB_SEEKER ||--o| HIRED_RECORD : "취업확정"
    COMPANY ||--o{ HIRED_RECORD : "소속됨"
```

##문제 2의 DB
```mermaid
erDiagram
```
