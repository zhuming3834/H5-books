```
#autocsdn.sh
#automatically send request to csdn blog

user=hyichao_csdn
articles='curl -s "http://blog.csdn.net/$user/" | grep 'href' | egrep -o "$user/articles/details/[[:digit:]]+" | sort | uniq'

for i in `seq 1000`

do

for article in $articles
  do
  curl -s "http://blog.csdn.net/zhuming3834/article/details/51111623" > /dev/null
  sleep 10
  echo "One Shot"
  done

echo $i

done
```

