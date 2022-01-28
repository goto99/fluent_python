# 1. Problems while using github and how to solve it.
## fatal: unable to access : Failed to connect to github.com port 443: Connection refused
Solution: step 1. try this command in cmd to find out my proxy.
          reg query "HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Internet Settings" | find /i "proxyserver"
          step 2. set the proxy information find out in git command.
          git config --global http.proxy http[s]://userName(encoded):password(encoded)@proxyaddress:port
          done!
