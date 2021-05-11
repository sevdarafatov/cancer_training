#Sevda Rafatov
#14.01.2019
#Project no:2

import statistics #importing statistics module
def splitCancerData(fileName): #defining a function with variable fileName
    try :
        
        file=open('cancerTrainingData.txt','r') #opening cancer training data
        d_tumor={} #opening an empty dictionary
        for line in file:
            if line.startswith('#'): #to get rid of the headers
                continue
            columns=line.rstrip().split(',') #dividing data into columns according to comma seperator
            tumorID=columns[0]               #first column of data which represents tumorID is assigned as tumorID
            d_tumor[tumorID]=columns[1:]     #columns of training data which each one represent an attribute assigned to according tumorID
        file.close()
        return d_tumor                       #return of the function is d_tumor
    except UnboundLocalError:
        print("A wrong mode used while opening file") #if definining mode of the handling the file will written false it will give an local error below
    except FileNotFoundError:
        print("File is not found,place data files and .py in the same folder")
def organizeCancerData(fileName): #defining a function to find average and midpoint of attributes in cancer training data
    try :
        d_tumor=splitCancerData(fileName)#function splitCancerData which was defined above is called

        sum_radius_M=0      #sum of radius attributes in each malignant tumor in training data
        sum_radius_B=0      #sum of radius attributes in each benign tumor in training data
        sum_texture_M=0     #sum of texture attributes in each malignant tumor in training data 
        sum_texture_B=0     #sum of texture attributes in each benign tumor in training data 
        sum_perimeter_M=0   #sum of perimeter attributes in each malignant tumor in training data
        sum_perimeter_B=0   #sum of perimeter attributes in each benign tumor in training data
        sum_area_M=0        #sum of area attributes in each malignant tumor in training data
        sum_area_B=0        #sum of area attributes in each benign tumor in training data
        sum_smoothness_M=0  #sum of smoothness attributes in each malignant tumor in training data
        sum_smoothness_B=0  #sum of smoothness attributes in each benign tumor in training data
        sum_compactness_M=0 #sum of compactness attributes in each malignant tumor in training data
        sum_compactness_B=0 #sum of compactness attributes in each benign tumor in training data
        sum_concavity_M=0   #sum of concavity attributes in each malignant tumor in training data
        sum_concavity_B=0   #sum of concavity attributes in each benign tumor in training data
        sum_concave_M=0     #sum of concave attributes in each malignant tumor in training data
        sum_concave_B=0     #sum of concave attributes in each benign tumor in training data
        sum_symmetry_M=0    #sum of symmetry attributes in each malignant tumor in training data
        sum_symmetry_B=0    #sum of symmetry attributes in each benign tumor in training data
        sum_fractal_M=0     #sum of fractal attributes in each malignant tumor in training data
        sum_fractal_B=0     #sum of fractal attributes in each benign tumor in training data
        counter_M=0         # counts the number of malignant tumors in training data
        counter_B=0         # counts the number of benign tumors in training data

        for key, value in d_tumor.items(): #The items() method returns a view object that displays a list of dictionary's (key, value) tuple pairs
            radius_mean=float(value[0])     #float value of first key from d_tumor dictionary assigned as radius_mean
            texture_mean=float(value[1])    #float value of second key from d_tumor dictionary assigned as texture_mean
            perimeter_mean=float(value[2])  #float value of third key from d_tumor dictionary assigned as perimeter_mean
            area_mean=float(value[3])       #float value of fourth key from d_tumor dictionary assigned as area_mean
            smoothness_mean=float(value[4]) #float value of fifth key from d_tumor dictionary assigned as smoothness_mean
            compactness_mean=float(value[5])#float value of sixth key from d_tumor dictionary assigned as compactness_mean
            concavity_mean=float(value[6])  #float value of seventh key from d_tumor dictionary assigned as concavity_mean
            concave_mean=float(value[7])    #float value of eight key from d_tumor dictionary assigned as concave_mean
            symmetry_mean=float(value[8])   #float value of nineth key from d_tumor dictionary assigned as symmetry_mean
            fractal_mean=float(value[9])    #float value of tenth key from d_tumor dictionary assigned as fractal_mean
            if value[-1]=='M': #if the last column of d_tumor is M
                sum_radius_M+=radius_mean #sum the values of radius_mean into sum_radius_M
                counter_M+=1              #increase the counter by one for each malignant tumor
                avg_radius_M=sum_radius_M/counter_M #find average radius of malignant tumors by dividing sum of radius of malignant tumors by number of malignant tumors in training data
            
                sum_texture_M+=texture_mean #sum the values of texture_mean into sum_texture_M
                avg_texture_M=sum_texture_M/counter_M #find average texture of malignant tumors by dividing sum of radius of malignant tumors by number of malignant tumors in training data

                sum_perimeter_M+=perimeter_mean       #same procedure goes on
                avg_perimeter_M=sum_perimeter_M/counter_M

                sum_area_M+=area_mean
                avg_area_M=sum_area_M/counter_M

                sum_smoothness_M+=smoothness_mean
                avg_smoothness_M=sum_smoothness_M/counter_M

        
                sum_compactness_M+=compactness_mean
                avg_compactness_M=sum_compactness_M/counter_M

                sum_concavity_M+=concavity_mean
                avg_concavity_M=sum_concavity_M/counter_M

                sum_concave_M+=concave_mean
                avg_concave_M=sum_concave_M/counter_M

                sum_symmetry_M+=symmetry_mean
                avg_symmetry_M=sum_symmetry_M/counter_M

                sum_fractal_M+=fractal_mean
                avg_fractal_M=sum_fractal_M/counter_M
        

        
            elif value[-1]=='B':                     #if the last column of d_tumor is M
                sum_radius_B+=radius_mean            #sum the values of radius_mean into sum_radius_B
                counter_B+=1                         #increase the benign tumor counter by one for each benign tumor
                avg_radius_B=sum_radius_B/counter_B  #find average radius of benign tumors by dividing sum of radius of benign tumors by number of benign tumors in training data

                sum_texture_B+=texture_mean          #same procedure goes on
                avg_texture_B=sum_texture_B/counter_B

                sum_perimeter_B+=perimeter_mean
                avg_perimeter_B=sum_perimeter_B/counter_B

                sum_area_B+=area_mean
                avg_area_B=sum_area_B/counter_B


                sum_smoothness_B+=smoothness_mean
                avg_smoothness_B=sum_smoothness_B/counter_B

            
                sum_compactness_B+=compactness_mean
                avg_compactness_B=sum_compactness_B/counter_B

                sum_concavity_B+=concavity_mean
                avg_concavity_B=sum_concavity_B/counter_B

                sum_concave_B+=concave_mean
                avg_concave_B=sum_concave_B/counter_B

                sum_symmetry_B+=symmetry_mean
                avg_symmetry_B=sum_symmetry_B/counter_B

                sum_fractal_B+=fractal_mean
                avg_fractal_B=sum_fractal_B/counter_B

        MalignantDictionary={'radius':avg_radius_M,'texture':avg_texture_M,'perimeter':avg_perimeter_M,'area':avg_area_M,'smoothness':avg_smoothness_M,'compactness':avg_compactness_M,'concavity':avg_concavity_M,'concave':avg_concave_M,'symmetry':avg_symmetry_M,'fractal':avg_fractal_M}
        #a dictionary to save average values of attributes of malignant tumors in training data    
        BenignDictionary={'radius':avg_radius_B,'texture':avg_texture_B,'perimeter':avg_perimeter_B,'area':avg_area_B,'smoothness':avg_smoothness_B,'compactness':avg_compactness_B,'concavity':avg_concavity_B,'concave':avg_concave_B,'symmetry':avg_symmetry_B,'fractal':avg_fractal_B}
        # a dictionary to save average values of attributes of benign tumors in training data
        midpointDictionary={k:statistics.mean([float(MalignantDictionary[k]),float(BenignDictionary[k])]) for k in MalignantDictionary}
        # for each attribute mean of MalignantDictionary value and BenignDictionary value are found and saved in midpointDictionary

        prettyPrint(MalignantDictionary,BenignDictionary,midpointDictionary)
        #prettyPrint function with variables MalignantDictionary,BenignDictionary and midpointDictionary which is defined below is called
        return(MalignantDictionary,BenignDictionary,midpointDictionary)
    except ValueError:
            print ("The value type of attributes should be float")    
    except ZeroDivisionError:
            print("Either counter_B or counter_M is equal to zero")



    
def prettyPrint(MalignantData,BenignData,midpointData): # a function prettyPrint is defined with variables MalignantData,BenignData and midpointData
    try:
        M=MalignantData
        B=BenignData
        mid=midpointData

        print("Key      Malignant   Classifier   Benign")
        print("         Average      Average     Average")
        print("radius     %10.3f%10.3f%10.3f" %(M['radius'],mid['radius'],B['radius']))#Values from MalignantData,midpointData and BenignData with key 'radius' are printed 
        print("texture    %10.3f%10.3f%10.3f" %(M['texture'],mid['texture'],B['texture']))#Values from MalignantData,midpointData and BenignData with key 'texture' are printed
        print("perimeter  %10.3f%10.3f%10.3f" %(M['perimeter'],mid['perimeter'],B['perimeter']))#Values from MalignantData,midpointData and BenignData with key 'perimeter' are printed
        print("area       %10.3f%10.3f%10.3f" %(M['area'],mid['area'],B['area']))#Values from MalignantData,midpointData and BenignData with key 'area' are printed
        print("smoothness %10.3f%10.3f%10.3f"%(M['smoothness'],mid['smoothness'],B['smoothness']))#Values from MalignantData,midpointData and BenignData with key 'smoothness' are printed
        print("compactness%10.3f%10.3f%10.3f"%(M['compactness'],mid['compactness'],B['compactness']))#Values from MalignantData,midpointData and BenignData with key 'compactness' are printed
        print("concavity  %10.3f%10.3f%10.3f"%(M['concavity'],mid['concavity'],B['concavity']))#Values from MalignantData,midpointData and BenignData with key 'concavity' are printed
        print("concave    %10.3f%10.3f%10.3f "%(M['concave'],mid['concave'],B['concave']))#Values from MalignantData,midpointData and BenignData with key 'concave' are printed
        print("symmetry   %10.3f%10.3f%10.3f"%(M['symmetry'],mid['symmetry'],B['symmetry']))#Values from MalignantData,midpointData and BenignData with key 'symmetry' are printed
        print("fractal    %10.3f%10.3f%10.3f"%(M['fractal'],mid['fractal'],B['fractal']))#Values from MalignantData,midpointData and BenignData with key 'fractal' are printed
        
    except KeyError:
        print("A key error occured,handle the key error.")
    

def testingPredictor (fileName,trainingData): #a function testingPredictor with two variables fileName and trainingData defined to classify the test set
    
    try:

        print("Reading in test data...") #test data will be read
        file=open(fileName,'r')
        dic_tumor={}                    #a new dictionary is opened to save test data
        list_last_column=[]             #a list opened to save the last column of test data
        for line in file:
            if line.startswith('#'):     #to get rid of the headers
                continue
            columns=line.rstrip().split(',') #dividing data into columns according to comma seperator
            tumorID=columns[0]               #first column of data which represents tumor ID is assigned as tumorID
            dic_tumor[tumorID]=columns[1:-1] #from second column till the last column of data assigned to the according tumor ID
            list_last_column.append(columns[-1]) #last column of data which shows B/M saved in list_last_column list
        file.close()
        print("Done reading test data.")
        print("Classifying records...")
        
        midpoint_list=list(trainingData.values()) #The method values() returns a list of all the values available in a given dictionary
        tumor_type=[] #an empty list to save the type of each tumor
        for key, value in dic_tumor.items():
            b_m_test="" #an empty string is opened
            for i in range(len(midpoint_list)): #in range of midpoint list
                if float(value[i])>=midpoint_list[i]: #if value of attribute in dic_tumor is higher or equal to value in midpoint list
                    b_m_test+='M'                     #assign this attribute as 'M'
                else:
                    b_m_test+='B'                     #otherwise assign this attribute as 'B'
            if b_m_test.count('M')>=5:                #if 5 or more than 5 attributes are assigned as 'M'           
                tumor_type+='M'                       #tumor type is 'M'
            else:
                tumor_type+='B'                       #otherwise tumor type is 'B'
        print("Done classifying.")
        counter=0
        for i in range(len(tumor_type)):              #in range of tumor type list
            if tumor_type[i]==list_last_column[i]:    #if item in list_last_column is equal to item in tumor_type list
                counter+=1                            #increase counter by one
            else:
                continue                   
        print("The classifier correctly predicted the class (malignant/benign)of%d records out of 231 records" %(counter))
        print("The classifier achieved an accuracy of %.2f percent."%((counter/231)*100))
        
    except IndexError:
        print("Handle the index error.")


def checkPatient(dataFile,midpointList): #a function checkPatient is defined with two variables dataFile and midpointList
    try :
              
        print("Reading in test data...")
        file=open(dataFile,'r')
        dic_tumor={}  #an empty dictionary opened
        list_last_column=[] #an empty list opened
        for line in file:
            if line.startswith('#'):        #to get rid of the header
                  continue
            columns=line.rstrip().split(',') #dividing data into columns according to comma seperator
            tumorID=columns[0]               #first column of data which represents tumor ID is assigned as tumorID
            dic_tumor[tumorID]=columns[1:-1] #from second column till the last column of data assigned to the according tumor ID
            list_last_column.append(columns[-1]) #last column of data which shows B/M saved in list_last_column list
        file.close()

        userInput=''                         #an empty string opened to save user input
        while userInput !='quit':            #while user input is not 'quit'
              userInput=input('Please enter a patient ID to check the status or type "quit" to stop:') #here user expected to input a patient ID or 'quit' to exit 
              if userInput=='quit':          #if user input is equal to 'quit'
                  print('Program finished.')
                  return

              patientData=dic_tumor[userInput] #patientData is assigned as a value to userInput key in dic_tumor dictionary
              patientData=[float(i) for i in patientData]
              tumor_type='' #an empty string to save Malignant or Benign for tumor
              i=0
              b_m_test=[] #an empty list to save Malignant or Benign for each attribute
              for each in patientData:

                  if float(each)>=list(midpointList.values())[i]: #if value of attribute in patientData is bigger than or equal to value in midpoinList
                      b_m_test.append('Malignant') #this attribute is assigned as 'Malignant'
                  else:
                      b_m_test.append('Benign')    #otherwise it is assigned as 'Benign'
                  i+=1
              
              if b_m_test.count('Malignant')>=5:   #if five or more of attributes assigned as 'Malignant' 
                  tumor_type='Malignant'           #the tumor is 'Malignant'
              else:
                  tumor_type='Benign'              #otherwise it is 'Benign'
              
              b_m_test.append(tumor_type)          #tumor_type is added to b_m_test list
              prettyPrint2(patientData,userInput,midpointList,b_m_test)
    except UnboundLocalError:
        print("A wrong mode used while opening file")
    except KeyError:
        print("Handle the key error occured")
    except ValueError:
        print("Handle the value error occured")



        
def prettyPrint2(PatientData, userInput, midpointData ,b_m_test): #function prettyPrint2 defined with parameters PatientData, userInput, midpointData and b_m_test        
    try:
        P=PatientData 
        mid=midpointData
        bmt=b_m_test 
        ID=userInput
              
        print("Checking ID:"+ID+"'s classification")
        print("Key            Patient   Classifier      Class")
        print("                Value    Cutoff          ")
        print("perimeter  %10.3f%10.3f%16.9s" %(P[2],mid['perimeter'],bmt[2]))  #third element in PatientData, value of key 'perimeter' in midpointData and third item in b_m_test are printed
        print("symmetry   %10.3f%10.3f%16.9s"%(P[8],mid['symmetry'],bmt[8]))    #nineth element in PatientData, value of key 'symmetry' in midpointData and nineth item in b_m_test are printed
        print("area       %10.3f%10.3f%16.9s" %(P[3],mid['area'],bmt[3]))       #fourth element in PatientData, value of key 'area' in midpointData and fourth item in b_m_test are printed
        print("concave    %10.3f%10.3f%16.9s "%(P[7],mid['concave'],bmt[7]))    #eight element in PatientData, value of key 'concave' in midpointData and eight item in b_m_test are printed 
        print("texture    %10.3f%10.3f%16.9s" %(P[1],mid['texture'], bmt[1]))   #second element in PatientData, value of key 'texture' in midpointData and second item in b_m_test are printed
        print("concavity  %10.3f%10.3f%16.9s"%(P[6],mid['concavity'],bmt[6]))   #seventh element in PatientData, value of key 'concavity' in midpointData and seventh item in b_m_test are printed
        print("radius     %10.3f%10.3f%16.9s" %(P[0],mid['radius'], bmt[0]))    #first element in PatientData, value of key 'radius' in midpointData and first item in b_m_test are printed
        print("compactness%10.3f%10.3f%16.9s"%(P[5],mid['compactness'],bmt[5])) #sixth element in PatientData, value of key 'compactness' in midpointData and third item in b_m_test are printed
        print("fractal    %10.3f%10.3f%16.9s"%(P[9],mid['fractal'], bmt[9]))    #tenth element in PatientData, value of key 'fractal' in midpointData and tenth item in b_m_test are printed
        print("smoothness %10.3f%10.3f%16.9s"%(P[4],mid['smoothness'],bmt[4]))  #fifth element in PatientData, value of key 'smoothness' in midpointData and fifth item in b_m_test are printed
        print("\nOverall Diagnosis for patient " + ID +": "+b_m_test[-1])       # last element of b_m_test is printed
    except KeyError:
        print("Handle the key error occured")
          

dataTrain=organizeCancerData('cancerTrainingData.txt') #function organizeCancerData is called
dataTest=testingPredictor('cancerTestingData.txt',dataTrain[2]) #dataTrain[2] is midpointDictionary
checkPatient('cancerTestingData.txt',dataTrain[2]) #dataTrain[2] is given as input to other functions          
        
    
          













          
