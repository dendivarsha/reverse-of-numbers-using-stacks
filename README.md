# this program is for getting reverse order of given numbers using stacks 
#inputs are taken by user
# Online Python compiler (interpreter) to run Python online.
# Write Python 3 code in this online editor and run
st=[]
def push(n):
    while(n!=0):
        st.append(n%10)
        n=int(n/10)
def revnum(n):
    push(n)
    reverse=0
    i=1
    while(len(st)>0):
        reverse=reverse + (st[len(st) - 1] * i)
        st.pop()
        i=i*10
    return reverse
n=int(input())
print(revnum(n))
#input=123
#output=321
#input=45678
#output=87654
