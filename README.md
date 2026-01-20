## Name: khellon patel

### Task 1: Hashing

**Reminder Deliverable:** Is your `salted-data.csv` in this repository?

Answer the following in this file:

* How many unique users are in the data?
  - 42

* How many salts did you create?
  - 42
  
* How many possible combinations will I need to try to figure out the secret ID
  of all students (assume I know all potential secret IDs and have your 
  `salted-data.csv`)
  - 1764 
  
* Instead of salts, if you were to use a nonce (unique number for each hashed
  field) how many possible combinations would I need to try?
  - 53,424
  
* Given the above, if this quiz data were *actual* class data, say for example
  your final exam, how would you store this dataset?  Why?
  - As per autual class data stoing student fname stoing in plain text i will store studen fname `salts + hash` to prevant to find user data 
  

```bash
salt="${USER_SALTS[$user_id]}"
    hash=$(printf "${salt}${user_id}" | sha256sum | awk '{print $1}')
```
