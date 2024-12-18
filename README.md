# Dawn_Bot

**original author**: Jaammerr  

from https://github.com/Jaammerr/The-Dawn-Bot

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
- Total maximum time per attempt: 3 minutes
- Total maximum time for all attempts: 9 minutes
- increase the time available for 2Captcha to resolve captchas
- **highly recommend to use 2Captcha's 100% verification function**, it can resolve the image much faster

### Implementation
- For implementation details, please refer to the original repository by Jaammerr. This implementation is identical to Jaammerr's repository, except for the addition of the Language.txt and userAgent.txt files.
