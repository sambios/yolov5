20210115
1. 导出jit.trace模型方法
   python3 ./model/export.py --weights yolov5s.pt

   执行完会输出yolov5s.torchscript.pt
2. 转bmodel
  import bmnetp
  bmnetp.compile(target="BM1684",
        model="./yolov5s.torchscript.pt",
        shapes=[[1,3,640,640]],
        outdir="./yolov5s_bmodel",
        opt=2
)




