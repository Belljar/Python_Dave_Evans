# Python_Dave_Evans
def freq_analysis(message):
  
    # Your code here
    distinct_list=[] #create empty list where you will update and maintain distinct numbers
    freq_list=[]    #create empty list where you will update frequency of each number
    for e in message:    #for each element in the list,check if it is there in the distinct list one by one
        if e not in distinct_list: #  if not there, update it in the distinct list, and update the frequency
            distinct_list.append(e)
            freq_list.append(1)
        else:
            freq_list[distinct_list.index(e)]=freq_list[distinct_list.index(e)]+1   #if in distinct list,just update the frequency, 
                                                                                      here the index of the number in distinct list 
                                                                                      is equal to the index of its frequency in frequency list
                                                                                     
    return distinct_list,freq_list
