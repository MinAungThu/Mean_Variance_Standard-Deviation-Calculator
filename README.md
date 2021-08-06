# Mean_Variance_Standard-Deviation-Calculator14



import numpy as np



def calculate(list):
    if len(list) != 9 :
       raise ValueError('List must contain nine numbers.')
    else :
      mtx=np.array(list).reshape((3,3))
      mean_list = [mtx.mean(0).tolist(),mtx.mean(1).tolist(),mtx.mean()]
      var_list= [mtx.var(0).tolist(),mtx.var(1).tolist(),mtx.var()]
      std_list = [mtx.std(0).tolist(),mtx.std(1).tolist(),mtx.std()]
      max_list = [mtx.max(0).tolist(),mtx.max(1).tolist(), mtx.max()]
      min_list = [mtx.min(0).tolist(),mtx.min(1).tolist(),mtx.min()]
      sum_list =[mtx.sum(0).tolist(),mtx.sum(1).tolist(),mtx.sum()]
      calculations = { 'mean' : mean_list  , 'variance' : var_list , 'standard deviation' : std_list , 'max' : max_list , 'min' : min_list , 'sum' : sum_list}
      
      
    return calculations

      


     


      
