# ����
1. data�ṩͳһ�����ݽӿڣ���traderʹ�ã������л�����Դ
���϶������Դ,Լ�����ݸ�ʽ������ͳһ�Ľӿڷ�����������µ�����Դ�������Լ����ʽ���ɽ��롣
����
(1)����֤ȯ�������ݿ�
(2)tushare
2. trader������Իز���live����
3. calendar���彻������
4. ./trader/strategy ������н��ײ���
5. ./trader/order ��������µ�����
6. ����ʹ�õĽӿ�api�����µ�����ѯ��ǰ�˻���Ϣ���ز�������ȹ��ܣ��ṩͳһ�Ľӿ�
7. signalSender�����ͽ����źŵ����䡢΢�ŵ�
8. optimizer����Թ�Ʊ�����������Ż�


# Լ��
## ��������
ģ����/�ļ���: event,signal_sender
����/����: get_data  
����: HistoryDataHandler  
����: historyDataHandler  
����: CONSTANT_VARIABLE  
����: this_is_a_variable  

## �ĵ���ʽ
'''
����˵����

Parameter
---------
....

Return
---------
....

'''

## data���ݽṹ

# �ܹ�
ʵ��BacktestEngine,���ݲ��Ա�д��initilize������handle_data������BacktestEngineʵ��������ʵ��start_backtest�����Իز���з�װ��

backtest_data_initilizer������ָ����������ʼ���ز�����Ľ������ݡ�Ϊ�ز��ṩ���ݽӿڡ�
context:����backtest_data_initilizer�����ݽӿ�,��blotter���н������ṩ��ѯ���µ������ս��׷����Ĺ��ܡ�
blotter:����backtest_data_initilizer�����ݽӿ�,��context���н������ṩ���ݽ������ݽ��д�ϵĹ��ܣ��ṩ�µ�ָ�����ͣ���ж����乲��������ǰcontextһ��������(�ռ�)��
recorder:���˻�״�����м�¼,�Խ���Ч������ͳ�ơ�
order:�ö����ṩ�Զ�����������

## ��Ŀ¼
constants:���峣��  
event�����������¼����ͣ����Ը��������岻ͬ���¼���  
data: �ṩ�ܹ�����������֧�֡�  
protfolio:�˻�  
protfolioHandler:�˻�ά��  
executioner:���  
performance:����  
riskManager:���  
optimizer:���Ż�  
backtest:�������ģ�飬ʵ�ֻز⹦��  
setting:���ϻز⡢live���ף��ṩ��װ��Ķ���ӿ�  

## ģ��
### data
#### tushareDatabase
�ṩ����tushare�����ݿⴴ����ά������ȡ�ȹ��ܵĽӿڡ������Լ�ǿ�����ݿ�Ĭ��ΪMySQL.

### strategy
strategy:�ṩ���Գ��󣬺����̳�  
multiFactorStrategy:�ṩ�����Ӳ��Գ��󣬺������Լ̳�  
sequentialFactorStrategy:�ṩ���ɸѡ���Գ���  

### calendar���彻������
calendar:�ṩ��������  


### out
#### bt
����ز���  
#### live
����live���  

### log
��־��

# �ƻ�
## 20170801
Ŀǰרע���ռ�زⲿ�֣��������ռ�ز���ٿ��Ƿ��Ӽ��ز⡣  
1. ��ɻ��ڹ���֤ȯ�������ݿ��dataģ�顣
2. ��ɻ�������ǰ��Ȩ���ݵĻز���򣬸�ģʽ�³ֲֹ�Ʊ����������ʵ�ʲ����ϡ�
3. �Ż�����api.
4. ��ɻ��ڲ���Ȩ�����Լ��ֺ��͹�ת�������ݵĻز�����ڸ�ģʽ��֧�ְ��տ��̼��µ���
5. ��ɻ���tushare��ʵʱ����ӿڣ�ʵ��live���׹���

# ������־

# �������
1. python2.7(Anaconda)
2. pymysql
3. tushare

## ˵��
