MemoryUtil

���¹��ܶ���32bits JVM��64bits JVM����ѹ��ָ�룬64bits JVM�ر�ѹ��ָ�붼���á�

MemoryUtil
���Ի�ö����shallowsize��
���Ի�ö����fullsize��
���Ի�ö����padding size��
���Ի�ö����full padding size��

MemoryDetailEntry��toString������
���Դ�ӡ�����������Ϣ��
��������ͷ������field��offset�ʹ�С��
padding��С��
���õĶ����������Ϣ��

allen.memoryutil.size
���Զ�̬������ͷ��С������ͨ������������
���Զ�̬������ô�С��
���Ի�û������ʹ�С��

���ʹ��
0 �鿴memoryutilĬ�����룬��jarĿ¼������ java -javaagent:memoryutil-0.1.jar -cp . allen.memoryutil.dirver.TestMemory��
1 ��memoryutil-0.1.jar�����̵�class path��
2 �����Լ�������࣬����Ϊtest.Allen������memoryutil�Ĺ������ӡ���Զ������Ϣ��
3 ��������ִ�� java -javaagent:memoryutil-0.1.jar -cp . test.Allen

����java�����ڴ�Ļ���֪ʶ����ο�
http://zhang-xzhi-xjtu.iteye.com/blog/2116304

"abcd"�ַ�������������

string abcd   //�����������û�����
----------------------------------------------------------------
object class info : java.lang.String                             //��������
object identityHashCode : 4875744                                //����identityHashCode
in parent info : root object
shallow size = 24                                                //����shallow size
full size = 48                                                   //����full size
full padding size = 4                                            //����full padding size
-----------shallow size detail.-----------------                 //����shallow size��������Ϣ
headerType = NormalHeader size = 8                               //��ͨ����ͷ����СΪ8
offset : 8 size = 4 private final char[] java.lang.String.value  //value field��offsetΪ8,��СΪ4��
offset : 12 size = 4 private final int java.lang.String.offset   //offset field��offsetΪ12,��СΪ4��
offset : 16 size = 4 private final int java.lang.String.count    //count field��offsetΪ16,��СΪ4��
offset : 20 size = 4 private int java.lang.String.hash           //hash field��offsetΪ20,��СΪ4��
padding size = 0                                                 //paddingΪ0��
-----------end of shallow size detail.----------
                                                                 //���ַ������õ�char[]������Ϣ
    object class info : char[]                                   
    object identityHashCode : 15672056                            
    in parent info : private final char[] java.lang.String.value in parent.  //�����ڱ����ö����е�λ����Ϣ��
    shallow size = 24
    full size = 24
    full padding size = 4
    -----------shallow size detail.-----------------
    headerType = ArrayHeader size = 12                           //�������ͷ����СΪ12
    compType = char arrayLength = 4 size = ( 2 * 4 ) = 8         //���������Ϊchar������Ϊ4����СΪ8��
    padding size = 4                                             //paddingΪ4��
    -----------end of shallow size detail.----------
----------------------------------------------------------------


