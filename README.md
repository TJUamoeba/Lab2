# ʵ��2�� 
Windows Form ʵ�� MIDI �����ļ��Ĳ���APP #
![��ͼ](https://github.com/TJUamoeba/Lab2/blob/master/Pictures/MainForm.png?raw=true)
## һ�� ���ܸ��� ##
�����AutoSizeFormClass�࣬���������AutoSizeChange�¼�������Ӧ�Ӷ��ﵽ�ؼ�����Ӧ�����С�Ĺ��� .
ʵ�ַ�����
1. �����ṹ��comStatus����¼һ���ؼ���ǰ����С���ڴ�������λ�ã�
2. �����б�compList����¼��ǰ��������пؼ���comStatus��
3. �������С�����仯ʱ������ControlAutoSize����. �ȶ�ȡ�б��ڼ�¼��������֮ǰ��״̬��Ϣ�����䵱ǰ��Ϣ�ȶԣ���ȡ���ڴ�С�仯�ı���ϵ����
	float wideScale = (float)mainForm.Width / (float)compList[0].Width;
                float highScale = (float)mainForm.Height / (float)compList[0].Height;
4. ����autoResize�������Դ����ڵ����пؼ�������һ����õı���ϵ�����б��ڼ�¼����һ��״̬��Ϣ���д�С��λ�õĵ���.
	subCtrl.Left = (int)((Left0) * wideScale);
                subCtrl.Top = (int)((Top0) * highScale);
                subCtrl.Width = (int)(Width0 * wideScale);
                subCtrl.Height = (int)(Height0 * highScale);
## ������Ŀ��ɫ ##
ʹ�ö���������ƿؼ�����ʹ�ù���
## ������������ ##
�ؼ�����Ӧ����120 + ��
## �ġ�����ʱ�� ##
�ؼ�����Ӧ���֣�3h
ѧϰ�߳�������⣺> 24h
## �塢ʵ����̼���� ##
1. �����ʵ��Ļ���Ҫ�󣺿ؼ�����Ӧ�����С��
2. ѧϰ���߳���ص�֪ʶ���������˽⻹�ǲ��㣬δ���ڱ���ʵ���м���Ӧ�ã�
3. ֮������ѧϰ�߳̿��Ƶ����֪ʶ���ֲ������֪ʶ©��.