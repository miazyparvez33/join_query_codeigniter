join this four table

Table A

id | isi a1 | isi a2

Table B

id | id_a | isi b1 | isi b2

Table C

id | id_a | isi c1 | isi c2

Table D

id | id_a | isi d1 | isi d2

Table E

id | id_a | isi e1 | isi e2


$this->db->select('BaseTbl.id, BaseTbl.tanggal, BaseTbl.atas_nama, BaseTbl.kerugian, BaseTbl.keterangan, BaseTbl.admin, BaseTbl.status');
$this->db->from('data_blacklist as BaseTbl',);
$this->db->join('bl_rekening as Rekening','Rekening.id_blacklist = BaseTbl.id','left');
$this->db->join('bl_telefon as Telefon','Telefon.id_blacklist = BaseTbl.id','left');
$this->db->join('bl_bukti as Bukti','Bukti.id_blacklist = BaseTbl.id','left');
$this->db->join('bl_pelapor as Pelapor','Pelapor.id_blacklist = BaseTbl.id','left');
