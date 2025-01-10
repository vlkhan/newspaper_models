1.u1 = User.objects.create_user('Artem') 
u2 = User.objects.create_user('Maksim') 

2.a = Author.objects.create(rating_au = 0.0, us_id = 1)   
a2 = Author.objects.create(rating_au = 0.0, us_id = 2) 

3.cat1 = Category.objects.create(name = 'Авто') 
cat2 = Category.objects.create(name = 'Экономика') 
cat3 = Category.objects.create(name = 'Наука')     
cat4 = Category.objects.create(name = 'Спорт') 

4. p1 = Post.objects.create(name = '"Спартак" уступил "Локомотиву" в матче КХЛ', tex
t = 'Встреча лидеров Западной конференции прошла в Ярославле в пятницу и завершилась со счетом 5:4 (4:1, 1:1, 0:2) в пользу хозяев. У ярославцев отличились Максим Шалунов (4-я минута), Степан Никулин (11), Никита Черепанов (13), Даниил Бут (14) и Александ
р Полунин (29). Спартаковцы ответили дублем Германа Рубцова (12, 41), а также шайбами Александра Пашина (22) и Андрея Локтионова (41).', rating = 0, news = 'st', author_i
d = 1)
p2 = Post.objects.create(name = 'ЦСКА всухую проиграл "Куньлуню" в матче КХЛ', text = 'Встреча прошла в пятницу в подмосковных Мытищах и завершилась со счетом 3:0 (1:0, 1:0, 1:0) в пользу хозяев. ', rating = 0, news = 'st', author_id = 1)             >>> p2 = Post.objects.create(name = '', text = 'Встреча прошла в пятницу в подмосковных Мытищах и завершилась со счетом 3:0 (1:0, 1:0, 1:0) в пользу хозяев. ', rating = 0, news = 'st', author_id = 1) 
p3 = Post.objects.create(name = 'Калининградские ученые предложили превратить мазут в экоуголь', text = 'Ученые Калининградского технического университета (КГТУ) предлагают обратить внимание на разработанные в вузе технологии, которые позволяют собранный на черноморском побережье мазут превратить в экоуголь, сообщает пресс-служба университета.', rating = 0, news = 'nw', author_id = 2) 

5.PostCategory.objects.create(post_id = 1, categ_id = 4)   
PostCategory.objects.create(post_id = 2, categ_id = 4)
PostCategory.objects.create(post_id = 3, categ_id = 2)              
PostCategory.objects.create(post_id = 3, categ_id = 3) 

6.
Comment.objects.create(text = 'Nice',rating_com =  0, post_c_id = 1, user_id = 2) 
Comment.objects.create(text = 'Good',rating_com =  0, post_c_id = 2, user_id = 2) 
Comment.objects.create(text = 'Well', rating_com =  0, post_c_id = 4, user_id = 1) 
Comment.objects.create(text = 'Wow', rating_com =  0, post_c_id = 2, user_id = 1)

7.p1.like()         
p2.like() 
p2.like()

8.Author.update_rating()

9.w1 = Author.objects.all().order_by('-rating_au').values('us_id', 'rating_au').first() 

10. pr = Post.objects.all().order_by('-rating').values('time_in', 'name', Post.preview() 'author_id').first()

11.q = Post.objects.filter(name = w10['name']).values('id').first() 
Comment.objects.filter(id = q['id']).values('time_com', 'text', 'rating_com', 'user_id')
