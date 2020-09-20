# Ivan Seviarynets
## mail: severinec7788@mail.ru, tel: +375295341017
3rd year student (VMSiS) BSUIR FKSiS. During his studies at the university he worked on various course projects from complex system programs in C, C++ to games and network applications in Java.
I always strive to learn something new in various areas of IT and am ready to work on interesting projects of varying degrees of complexity.

Sample code from react app "social-network":
```
import React from 'react';
import s from './MyPosts.module.css';
import Post from './Post/Post';
import { addPostActionCreator, updateNewPostTextActionCreator } from '../../../redux/profile-reducer';

const MyPosts = (props) => {
  let newPostElement = React.createRef();

  let onAddPost = () => {
    props.addPost();
  }

  let onPostChange = () => {
    let text = newPostElement.current.value;
    props.updateNewPostText(text)
  }

  let postsElements = props.posts.map(p => <Post message={p.message} key={p.id} likesCount={p.likesCount} />);
  return <div>
    <h3>My posts</h3>
    <div>
      <textarea onChange={onPostChange} ref={newPostElement} value={props.newPostText}></textarea>
      <button onClick={onAddPost}>Add post</button>
    </div>
    <div className={s.posts}>
      {postsElements}
    </div>
  </div>
}
export default MyPosts;
```

Work examples:
* Computer remote control software (Linux): https://github.com/sever7788/course_works
* 2D Game Pacman: https://github.com/sever7788/KPP

He graduated from the Rechitsa regional lyceum (physics and mathematics). At the moment, a student at BSUIR, future specialty systems engineer.
Beginner English level.
