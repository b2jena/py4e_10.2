name = input("Enter file:")
if len(name) < 1 : name = "mbox-short.txt"
handle = open(name)
counts={}
for line in handle:
    line=line.rstrip()
    if not line.startswith('From'): continue
    words=line.split()
    words=words[5:6]
    for word in words:
        we=word.split(":")
        we=we[0]
        if we in counts:
            counts[we]+=1
        else:
            counts[we]=1
st= list()
for word, counts in counts.items():
    newtup=(word, counts)
    st.append(newtup)
st= sorted(st,)
for word, counts in st:
    print(word, counts)
