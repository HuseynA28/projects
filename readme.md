# Python Local Mühitinin Qurulması Üçün Təlimat

Bu sənəd, yerli kompüterinizdə Python mühitini qurmaq və data analitik ası üçün lazım olan alətləri quraşdırmaq üçün addım-addım bələdçidir. Aşağıdakı təlimatları izləyərək öz kodunuzu rahatlıqla işlədə bilərsiniz.

## Addım 1: Python Quraşdırılması

Əğər kodunuzu yerli kompüterdə istifadə etmək istəyirsinizsə, ilk olaraq Python quraşdırmalısınız.

1. Python-un ən son versiyasını [rəsmi Python veb səhifəsindən](https://www.python.org/downloads/) endirin.
2. Quraşdırma zamanı **"Add Python to PATH"** seçimini aktiv etməyi unutmayın. Bu, Python-u terminaldan istifadə etmək üçün vacibdir.
3. Quraşdırma tamamlandıqdan sonra, terminalda Python-un quraşdırıldığını yoxlamaq üçün aşağıdakı əmri işlədin:

   ```sh
   python --version
   ```

## Addım 2: Virtual Environment Yaratmaq

Virtual environment (virtual mühit), layihələriniz üçün izole edilmiş bir Python mühiti yaradır. Bu, fərqli layihələrin bir-birinə təsir etməməsini təmin edir.

**"dataAnalytics"** adında bir virtual environment yaratmaq üçün:

1. Terminalı açın (*Windows-da Command Prompt və ya PowerShell, Unix-like sistemlərdə Terminal*).
2. Aşağıdakı əmri işlədin:

   ```sh
   python -m venv dataAnalytics
   ```

Bu əmr, cari qovluqda **"dataAnalytics"** adında bir virtual environment yaradacaq.

## Addım 3: Virtual Environment-i Aktivləşdirmək

Virtual environment-i istifadə etmək üçün onu aktivləşdirmək lazımdır. Aktivləşdirmə əmri əməliyyat sistemindən asılı olaraq dəyişir:

**Windows-da:**

```sh
dataAnalytics\Scripts\activate
```

**Unix-like sistemlərdə (Linux, macOS):**

```sh
source dataAnalytics/bin/activate
```

Aktivləşdirildikdən sonra terminalda virtual environment-in adını görəcəksiniz, məsələn: **(dataAnalytics)**. Bu, virtual mühitin aktiv olduğunu göstərir.

## Addım 4: `requirements.txt` Faylından Paketləri Yükləmək

Layihəniz üçün lazım olan paketləri `requirements.txt` faylından quraşdırmaq üçün:

1. Virtual environment-in aktiv olduğundan əmin olun.
2. Terminalda aşağıdakı əmri işlədin:

   ```sh
   pip install -r requirements.txt
   ```

Bu əmr, `requirements.txt` faylında sadalanan bütün paketləri virtual environment-ə quraşdıracaq. Əğər faylda **pandas, numpy** kimi data analitik ası paketləri varsa, onlar avtomatik yüklənəcək.