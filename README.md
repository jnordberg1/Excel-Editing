# -*- coding: utf-8 -*-
"""
Created on Tue Jul 17 13:09:16 2018

@author: JacobNordberg
"""
#DELETE THE FIRST ROW CONTAINING "[STATE INITIALS] Postcard List"  
#import pandas
import pandas

#original file
data = pandas.read_excel('FILE PATH TO XLS FROM ZOHO', 0)

#dropping rows (axis = 0 is used for horizonal dropping)
data.drop([662,663,664], axis=0, inplace=True)

#dropping columns (axis = 1 is for vertical
data.drop(['LEADID','Company'], axis=1, inplace=True)

#new file being created
data.to_csv('OUTPUT FILE PATH AND FILE NAME')

#DELETE COLUMN 'A'
#ADD IN YOUR NAME AND THE OFFICE ADDRESS AND YOUR NAME AND YOUR HOME ADDRESS
#SAVE AS .XLSX FOR SIR SPEEDY
