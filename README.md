from PyQt4.QtGui import *
from PyQt4.QtCore import *

class notHesaplama(QDialog):
    def __init__(self,ebeveyn=None):
        super(notHesaplama,self).__init__(ebeveyn)
        grid=QGridLayout()
        grid.addWidget(QLabel('Arasınav:'),0,0)
        self.arasinav=QLineEdit()
        grid.addWidget(self.arasinav,0,1)
        grid.addWidget(QLabel('Yarıyılsonu Sınavı:'),1,0)
        self.yariyilsonusinavi=QLineEdit()
        grid.addWidget(self.yariyılsonusinavi,1,1)
        grid.addWidget(QLabel('Bütünleme Notu:'),2,0)
        self.butunlemenotu=QLineEdit()
        grid.addWidget(self.butunlemenotu,2,1)
        ortalama=QPushButton('Ortalama')
        grid.addWidget(ortalama,3,0,1,2)
        self.setLayout(grid)
        self.setWindowTitle('Not Ortalama Penceresi')
        self.connect(hesaplaTusu,SIGNAL('pressed()',self.ortalama)
  def ortalama(self):
        self.arasinav=int(self.arasinav.text())
        self.yariyilsonusinav=int(self.yariyilsonusinav.text())
        self.butunlemenotu=int(self.butunlemenotu.text())
                     

    uyg=QApplication([])
    pencere=notortalama()
    pencere.show()
    uyg.exec_                 
