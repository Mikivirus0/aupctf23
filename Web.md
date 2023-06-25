## Challenge Name: Starter
mera tu sir chakra raha tum dekh lo ... 
Link: https://challs.aupctf.live/starter/\
## Sol:
So There  were scrambled chars on screen:
![image](https://github.com/Mikivirus0/aupctf23/assets/85563293/5175d460-ac7b-4f43-9390-7127171890c8)
### So checked sourcecode:
![image](https://github.com/Mikivirus0/aupctf23/assets/85563293/2814edb1-ff1e-46b6-adee-eb827824c783)
Here's flag. 
From Up to Down 
### Flag: aupCTF{w45n't-th47-h4rd-r1gh7}

## Challenge Name: SQLi - 1
Link: https://challs.aupctf.live/sqli-1/
## Sol:
Well, i tried manual brutforcing with knwon payloads of SQL Injection and got this one working: ```' OR 1 -- -```
![image](https://github.com/Mikivirus0/aupctf23/assets/85563293/c1ca05a6-1e20-47a0-b509-1a57ba202d41)
### And i got flag.
![image](https://github.com/Mikivirus0/aupctf23/assets/85563293/bccc9f8f-5dc6-4f0a-a18f-9fb37a350826)

### Flag: aupCTF{3a5y-sql-1nj3cti0n}

## Challenge Name: SQLi - 2
Link: https://challs.aupctf.live/sqli-2/
## Sol:
Well Again SQL Injection...! 
I just tried same paylaod and got flag lmao. ```' OR 1 -- -```
![image](https://github.com/Mikivirus0/aupctf23/assets/85563293/c1ca05a6-1e20-47a0-b509-1a57ba202d41)
### And i got flag.
![image](https://github.com/Mikivirus0/aupctf23/assets/85563293/4569e4d5-a69d-4187-83eb-77d93c15f7b9)
## Flag: aupCTF{m3d1um-sql-1nj3cti0n}

## Challenge Name: Directory
The flag is buried in one of the directory. 
## Sol:
![image](https://github.com/Mikivirus0/aupctf23/assets/85563293/470d476c-ef2e-4749-96f2-3ba0a1ef15a5)

I made a python script to scrape all dirs and at the end i just searched for "aup" in saved file.
```
import requests
base_url = "https://challs.aupctf.live/dir/page/"
start_page = 545
end_page = 1000
file_path = "directory_data.txt"
file = open(file_path, "w")
for page in range(start_page, end_page + 1):
    url = base_url + str(page)

    response = requests.get(url)
    if response.status_code == 200:
        file.write(f"--- Page {page} ---\n")
        file.write(response.text)
        file.write("\n\n")
        print(f"Data from Page {page} saved.")
    else:
        print(f"Failed to retrieve data from Page {page}.")

# Close the file
file.close()
print("All directory data saved to", file_path)
```

And it gave me flag in 5 minutes on Page 712.
## Flag: aupCTF{d1r3ct0r13s-tr1v14l-fl4g}








