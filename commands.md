### find which jar contains the class when you have a lot of jars to search through locally
while read line; do unzip -l $line | grep -H -i "${SEARCH_CLASS}" && echo $line ; done < <(find ${SEARCH_DIR}  -name '*.jar')
