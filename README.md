<html>
<head>
<title>Pendaftaran</title>
</head>

<body>
<form method="post">
<table border="0">
<tr>
    <td> Nama Mahasiswa </td>
    <td> : </td>
    <td colspan="7"> <input type="text" name="nama" size="54"/> </td>
</tr>
<tr>
    <td> NIM </td>
    <td> : </td>
    <td colspan="7"> <input type="text" name="nim"/></td>
</tr>
<tr>
    <td> Tempat Lahir </td>
    <td> : </td>
    <td colspan="7"> <input type="text" name="tempat" /></td>
</tr>
<tr>
    <td> Tanggal Lahir </td>
    <td> : </td>
    <td> <input type="text" name="tanggal" size="10"/> </td>
    <td> Bulan </td>
    <td> : </td>
    <td><select name="bulan">
        <option value="1" selected="selected"> Jan </option>
        <option value="2" > Feb </option>
        <option value="3" > Mar </option>
        <option value="4" > Apr </option>
        <option value="5" > Mei </option>
        <option value="6" > Jun </option>
        <option value="7" > Jul </option>
        <option value="8" > Agu </option>
        <option value="9" > Sep </option>
        <option value="10" > Okt </option>
        <option value="11" > Nov </option>
        <option value="12" > Des </option></select></td>
    <td> Tahun </td>
    <td> : </td>
    <td> <input type="text" name="tahun" size="10" /> </td>       
</tr>
<tr>
    <td> Jenis Kelamin </td>
    <td> : </td>
    <td colspan="7"> <select name="kelamin">
                    <option value="1" selected="selected"> - </option>
                    <option value="2"> Laki-Laki </option>
                    <option value="3"> Perempuan </option></select></td>
</tr>
<tr>
    <td> Alamat </td>
    <td> : </td>
    <td colspan="7"><textarea name="alamat" cols="41" rows="7"></textarea></td>
</tr>
<tr>
    <td colspan="9" align="right"><input type="submit" name="submit" value="Simpan" /><input type="reset" name="reset" value="Batal" /></td>
</tr>
</table>
</body>
</html>

<?php
$nama=isset($_POST['nama'])?$_POST['nama']:'';
$nim=isset($_POST['nim'])?$_POST['nim']:'';
$tempat=isset($_POST['tempat'])?$_POST['tempat']:'';
$tanggal=isset($_POST['tanggal'])?$_POST['tanggal']:'';
$bulan=isset($_POST['bulan'])?$_POST['bulan']:'';
$tahun=isset($_POST['tahun'])?$_POST['tahun']:'';
$kelamin=isset($_POST['kelamin'])?$_POST['kelamin']:'';
$alamat=isset($_POST['alamat'])?$_POST['alamat']:'';

if(!empty($nama) and !empty($nim) and !empty($tempat) and !empty($tanggal) and !empty($bulan) and !empty($tahun) and !empty($kelamin) and !empty($alamat))
{
    ?>
<table border="1">
<tr>
    <td> Nama Mahasiswa </td>
    <td> : </td>
    <td colspan="7">
        <?php 
        if (!empty($nama))
            {
                echo $nama ;
            }
        else 
            {   
            echo"<script>alert('Masukkan Nama')</script>";
            }
        ?>
</tr>
<tr>
    <td> NIM </td>
    <td> : </td>
    <td colspan="7"><?php echo $nim ?></td>
</tr>
<tr>
    <td> Tempat Lahir </td>
    <td> : </td>
    <td colspan="7"><?php echo $tempat ?></td>
</tr>
<tr>
    <td> Tanggal Lahir </td>
    <td> : </td>
    <td> <?php echo $tanggal ?> </td>
    <td> Bulan </td>
    <td> : </td>
    <td>
    <?php 
    if($bulan=="1")
        {
            echo "Januari";
        }
    else if($bulan=="2")
        {
            echo "Februari";
        }
    else if($bulan=="3")
        {
            echo "Maret";
        }
    else if($bulan=="4")
        {
            echo "April";
        }
    else if($bulan=="5")
        {
            echo "Mei";
        }
    else if($bulan=="6")
        {
            echo "Juni";
        }
    else if($bulan=="7")
        {
            echo "Juli";
        }
    else if($bulan=="8")
        {
            echo "Agustus";
        }
    else if($bulan=="9")
        {
            echo "September";
        }
    else if($bulan=="10")
        {
            echo "Oktober";
        }
    else if($bulan=="11")
        {
            echo "November";
        }
    else if($bulan=="12")
        {
            echo "Desember";
        }
    else
        {
            echo "Salah";
        }
    ?>
    </td>
    <td> Tahun </td>
    <td> : </td>
    <td> <?php echo $tahun ?> </td>       
</tr>
<tr>
    <td> Jenis Kelamin </td>
    <td> : </td>
    <td colspan="7"><?php echo $kelamin ?></td>
</tr>
<tr>
    <td> Alamat </td>
    <td> : </td>
    <td colspan="7"><?php echo $alamat ?></td>
</tr>
</table>
<?php
}
else
{
    echo"<script>alert('Data Kosong')</script>";
}
?>

<font color="red"><h3>Ysabtian.blogspot.com</h3></font>