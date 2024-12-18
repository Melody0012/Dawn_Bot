# Dawn_Bot

**original author**: Jaammerr  

https://github.com/Jaammerr/The-Dawn-Bot

  
# Changes

## Configuration Changes

### Added New Configuration Files
1. `config/data/Language.txt`
   - Contains language preferences for each account
   - Format: `language_code,en;q=0.9` (e.g., `it,en;q=0.9`) 
   - Each line corresponds to the same index in userAgent.txt
   - Helps avoid detection by using varied language preferences

2. `config/data/userAgent.txt`
   - Contains User-Agent strings for each account
   - Each line corresponds to a specific account
   - Format example:
     ```
     Mozilla/5.0 (Windows NT 10.0; Win64; x64) Chrome/123.0.0.0 Safari/537.36
     Mozilla/5.0 (Windows NT 10.0; Win64; x64) Chrome/122.0.0.0 Safari/537.36
     ```
   - Maintains consistent browser fingerprint per account

## Enhanced Captcha Solving

### Improved 2Captcha Configuration
- Extended timeout from 60s to 180s (3 minutes) per attempt
- Each account gets 3 attempts to solve captcha
- Checks result every 5 seconds (36 checks per attempt)
- Total maximum time per attempt: 180 seconds
- Total maximum time for all attempts: 9 minutes

## Header Flexibility Improvements

### Dynamic Header System
- Headers matched by index between User-Agent and Language
- Consistent identity per account across all requests
- Reduces detection through pattern matching
