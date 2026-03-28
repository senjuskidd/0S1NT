
# FSB Part 1.
```
## Context

A historical dataset linked to an **FSB-related leak** contains partial civil information.  
Only the individual’s identity is visible. The date of birth is missing.

## Known Information

- **Full name:** КОВЖАРОВА ЕЛЕНА АЛЕКСАНДРОВНА
- **Gender:** Female

## Objective

Using open-source intelligence methods, determine the **date of birth** of the individual.

No direct access to private databases or accounts is permitted.

### Flag format


OSINT{DD/MM/YYYY}
```

Name: КОВЖАРОВА ЕЛЕНА АЛЕКСАНДРОВНА
Gender: Female

## Foot Printing
Name Search We [Find](https://nationalsecuritynews.com/2022/06/ukraine-intelligence-publishes-names-of-620-russian-agents/) Her Date of Birth as 11/12/1968
![[Pasted image 20260328135034.png]]
# FSB Part 2.
```
## Context

A separate dataset references the same individual but contains only a **digital contact identifier**.  
Other personal identifiers were removed.

## Known Information

- **Email address:** polinaak@rambler.ru

This email address appears across multiple historical data sources.

## Objective

Using passive OSINT correlation, identify the **national social security identifier (SNILS)** associated with the individual.

### Flag format


OSINT{SNILS_NUMBER}
```

Email: polinaak@rambler.ru

## Foot Printing
We need National Social Security Identifier(SNILS) which according to [Wikipedia](https://en.wikipedia.org/wiki/SNILS_(Russia)) is a 11-digit unique required for Pension Fund of the Russian Federation and is used universally as a primary personal number within the Government of Russia.

We need to Find a *Historical Data Source* Most probably a leak where the digital contact identifier would be her email - polinaak@rambler.ru

Seems like applications go through the [Public Service Portal](https://www.gosuslugi.ru/)

Found This Telegram Bot @leaks_db_search_bot where you can search with email and find leaked info 
SNILS: 03262656135
![[Pasted image 20260328142826.png]]

# FSB Part 3.
```
## Context

Archived online records indicate that personal identifiers were reused across social platforms.  
The profile itself is not directly named.

## Known Information

- **Email address:** [polinaak@rambler.ru](mailto:polinaak@rambler.ru)
- **Phone number:** +7 910 438 8202

## Objective

Identify the **VK social network profile** historically associated with these identifiers.

---

## Rules (Apply to All Challenges)

- Passive OSINT techniques only
- No interaction with accounts or individuals
- No authentication or recovery attempts
- Educational and analytical use exclusively

### Flag format


OSINT{VK_ID}
```

Well we have the phone number we are going to use the bot from step 2 again but using the phone number this time.

![[Pasted image 20260328162552.png]]Try every single one and the highlighted one works
![[Pasted image 20260328162724.png]]

