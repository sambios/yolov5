20210115
1. ����jit.traceģ�ͷ���
   python3 ./model/export.py --weights yolov5s.pt

   ִ��������yolov5s.torchscript.pt
2. תbmodel
  import bmnetp
  bmnetp.compile(target="BM1684",
        model="./yolov5s.torchscript.pt",
        shapes=[[1,3,640,640]],
        outdir="./yolov5s_bmodel",
        opt=2
)




